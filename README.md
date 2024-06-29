# Almanam Entities.   
----------------------------------------------------------------------------------------------------
Without Dream comment module & without profile modification entity in user Module

## Auth
---------------------

### Auth Enumerations
---------------------

##### Gender

| **Field Label** | **Field Name** | 
|-----------------|----------------|
| `male`          | `1`            |
| `female`        | `2`            |

### Auth Parameters
---------------------

##### LoginCredentials (api/v1/login)

| **Field Label** | **Field Name** | **Field gType** | **Required/Optional** |
|-----------------|----------------|-----------------|-----------------------|
| `email`         | `email`        | `String`        | Required              |
| `password`      | `password`     | `String`        | Required              |

##### LogoutParameters (api/v1/logout)

| **Field Label** | **Field Name** | **Field Type** | **Required/Optional** |
|-----------------|----------------|----------------|-----------------------|
| `fcmToken`      | `token`        | `String`       | Required              |

##### OtpConfirmationParameters (api/v1/check-reset-password-otp)

| **Field Label** | **Field Name** | **Field Type** | **Required/Optional** |
|-----------------|----------------|----------------|-----------------------|
| `otp`           | `otp`          | `String`       | Required              |
| `phone`         | `phone`        | `String`       | Optional              |
| `email`         | `email`        | `String`       | Optional              |

##### PasswordResetRequestParameters (api/v1/forget-password)

| **Field Label** | **Field Name** | **Field Type** | **Required/Optional** |
|-----------------|----------------|----------------|-----------------------|
| `phone`         | `phone`        | `String`       | Optional              |
| `email`         | `email`        | `String`       | Optional              |

##### RegisterCredentials (api/v1/register)

| **Field Label**        | **Field Name**          | **Field Type** | **Required/Optional** |
|------------------------|-------------------------|----------------|-----------------------|
| `bio`                  | `bio`                   | `String`       | Optional              |
| `birthDay`             | `birthday`              | `DateTime`     | Optional              |
| `countryId`            | `country_id`            | `int`          | Required              |
| `email`                | `email`                 | `String`       | Required              |
| `firstName`            | `first_name`            | `String`       | Required              |
| `gender`               | `gender`                | `int`          | Optional              |
| `lastName`             | `last_name`             | `String`       | Required              |
| `password`             | `password`              | `String`       | Required              |
| `passwordConfirmation` | `password_confirmation` | `String`       | Required              |
| `phone`                | `phone`                 | `String`       | Optional              |

##### ResetPasswordParameters (api/v1/reset-password)

| **Field Label**        | **Field Name**          | **Field Type** | **Required/Optional** |
|------------------------|-------------------------|----------------|-----------------------|
| `otp`                  | `otp`                   | `String`       | Required              |
| `email`                | `email`                 | `String`       | Optional              |
| `password`             | `password`              | `String`       | Required              |
| `passwordConfirmation` | `password_confirmation` | `String`       | Required              |
| `phone`                | `phone`                 | `String`       | Optional              |

##### SocialMediaCredentials (api/v1/social/auth)

| **Field Label** | **Field Name** | **Field Type** | **Required/Optional** |
|-----------------|----------------|----------------|-----------------------|
| `token`         | `token`        | `String`       | Required              |
| `socialMedia`   | `method_id`    | `int`          | Required              |

## Banner
---------------------

### Banner Entity
---------------------

##### ContactUsAdBanner

| **Field Label** | **Field Name** | **Field gType** | **Required/Optional** |
|-----------------|----------------|-----------------|-----------------------|
| `id`            | `id`           | `int`           | Required              |
| `image`         | `image`        | `String`        | Required              |
| `name`          | `name`         | `String`        | Required              |
| `type`          | `type`         | `int`           | Required              |

##### NoneAdBanner

| **Field Label** | **Field Name** | **Field gType** | **Required/Optional** |
|-----------------|----------------|-----------------|-----------------------|
| `id`            | `id`           | `int`           | Required              |
| `image`         | `image`        | `String`        | Required              |
| `name`          | `name`         | `String`        | Required              |
| `type`          | `type`         | `int`           | Required              |

##### RelationalAdBanner

| **Field Label** | **Field Name** | **Field gType** | **Required/Optional** |
|-----------------|----------------|-----------------|-----------------------|
| `id`            | `id`           | `int`           | Required              |
| `image`         | `image`        | `String`        | Required              |
| `name`          | `name`         | `String`        | Required              |
| `type`          | `type`         | `int`           | Required              |
| `target`        | `target`       | `int`           | Required              |
| `targetType`    | `target_type`  | `int`           | Required              |

##### UrlAdBanner

| **Field Label** | **Field Name** | **Field gType** | **Required/Optional** |
|-----------------|----------------|-----------------|-----------------------|
| `id`            | `id`           | `int`           | Required              |
| `image`         | `image`        | `String`        | Required              |
| `name`          | `name`         | `String`        | Required              |
| `type`          | `type`         | `int`           | Required              |
| `url`           | `url`          | `String`        | Required              |

### Banner Enumerations
---------------------

##### TargetType

| **Field Label** | **Field Name** | 
|-----------------|----------------|
| `PUSHMESSAGE`   | `1`            |
| `BLOG`          | `2`            |
| `DREAM`         | `3`            |
| `PACKAGE`       | `4`            |
| `EXPERT`        | `5`            |
| `CONTACTUS`     | `6`            |
| `COMMENT`       | `7`            |
| `DREAMCOMMENT`  | `8`            |
| `PAYMENT`       | `9`            |

##### BannerType

| **Field Label** | **Field Name** | 
|-----------------|----------------|
| `RELATION`      | `1`            |
| `URL`           | `2`            |
| `NONE`          | `3`            |
| `CONTACTUS`     | `4`            |

## Blog
---------------------

### Blog Entity
---------------------

##### Blog

| **Field Label** | **Field Name**   | **Field Type**    | **Required/Optional** |
|-----------------|------------------|-------------------|-----------------------|
| `commentsCount` | `comments_count` | `int`             | Required              |
| `content`       | `content`        | `String`          | Required              |
| `createdAt`     | `created_at`     | `DateTime`        | Required              |
| `expert`        | `expert`         | `Object`          | Required              |
| `id`            | `id`             | `int`             | Required              |
| `image`         | `image`          | `String`          | Optional              |
| `isFavourite`   | `is_favourite`   | `bool`            | Required              |
| `isLiked`       | `is_liked`       | `bool`            | Required              |
| `likes`         | `likes`          | `int`             | Required              |
| `title`         | `title`          | `int`             | Required              |
| `video`         | `video`          | `Array Of Object` | Optional              |

##### Blog Video

| **Field Label** | **Field Name** | **Field Type** | **Required/Optional** |
|-----------------|----------------|----------------|-----------------------|
| `id`            | `id`           | `int`          | Required              |
| `url`           | `url`          | `String`       | Required              |

## BlogComment
---------------------

### BlogComment Entity
---------------------

##### BlogComment

| **Field Label** | **Field Name**  | **Field Type**       | **Required/Optional** |
|-----------------|-----------------|----------------------|-----------------------|
| `comment`       | `comment`       | `String`             | Required              |
| `createdAt`     | `created_at`    | `DateTime`           | Required              |
| `id`            | `id`            | `int`                | Required              |
| `likes`         | `likes`         | `int`                | Required              |
| `parent`        | `parent`        | `BlogComment Object` | Optional              |
| `repliesCount`  | `replies_count` | `int`                | Required              |
| `user`          | `user`          | `User Object`        | Required              |

### BlogComment Enumerations
---------------------

##### BlogCommentType

| **Field Label** | **Field Name** | 
|-----------------|----------------|
| `commentReplay` | `1`            |
| `comment`       | `2`            |

### BlogComment Parameters
---------------------

##### BlogCommentsParameters (api/v1/blog/comments/7)

| **Field Label** | **Field Name** | **Field gType** | **Required/Optional** |
|-----------------|----------------|-----------------|-----------------------|
| `blogId`        | `id`           | `int`           | Required              |
| `page`          | `page`         | `int`           | Required              |
| `limit`         | `perPage`      | `int`           | Required              |
| `sortBy`        | `sortKey`      | `String`        | Optional              |
| `sortType`      | `sortType`     | `String`        | Optional              |

##### BlogCommentCreationParameters (api/v1/comments)

| **Field Label**   | **Field Name** | **Field gType** | **Required/Optional** |
|-------------------|----------------|-----------------|-----------------------|
| `comment`         | `comment`      | `String`        | Required              |
| `id`              | `id`           | `int`           | Required              |
| `BlogCommentType` | `type`         | `int`           | Required              |

##### BlogCommentRepliesParameters (api/v1/comments/7/replies)

| **Field Label** | **Field Name** | **Field gType** | **Required/Optional** |
|-----------------|----------------|-----------------|-----------------------|
| `id`            | `id`           | `int`           | Required              |
| `page`          | `page`         | `int`           | Required              |
| `limit`         | `perPage`      | `int`           | Required              |
| `sortBy`        | `sortKey`      | `String`        | Optional              |
| `sortType`      | `sortType`     | `String`        | Optional              |

## ContactUs
---------------------

### ContactUs Entity
---------------------

##### ContactUs

| **Field Label** | **Field Name** | **Field Type** | **Required/Optional** |
|-----------------|----------------|----------------|-----------------------|
| `createdAt`     | `created_at`   | `DateTime`     | Required              |
| `id`            | `id`           | `int`          | Required              |
| `email`         | `email`        | `String`       | Required              |
| `message`       | `message`      | `String`       | Required              |
| `name`          | `name`         | `String`       | Required              |
| `phone`         | `phone`        | `String`       | Required              |

### ContactUs Parameters
---------------------

##### SendContactUsParameters (api/v1/contact-us)

| **Field Label** | **Field Name** | **Field gType**   | **Required/Optional** |
|-----------------|----------------|-------------------|-----------------------|
| `countryId`     | `country_id`   | `int`             | Required              |
| `email`         | `email`        | `String`          | Required              |
| `images`        | `images`       | `Array of String` | Required              |
| `message`       | `message`      | `String`          | Required              |
| `name`          | `name`         | `String`          | Required              |
| `phone`         | `phone`        | `String`          | Required              |

## Country
---------------------

### Country Entity
---------------------

##### Country

| **Field Label**   | **Field Name**     | **Field Type** | **Required/Optional** |
|-------------------|--------------------|----------------|-----------------------|
| `countryCode`     | `country_code`     | `String`       | Required              |
| `defaultLanguage` | `default_language` | `String`       | Required              |
| `id`              | `id`               | `int`          | Required              |
| `name`            | `name`             | `String`       | Required              |
| `phonePattern`    | `phone_pattern`    | `String`       | Required              |
| `phonePrefix`     | `phone_prefix`     | `String`       | Required              |
| `phoneLength`     | `phone_length`     | `int`          | Required              |

## Dream
---------------------

### Dream Entity
---------------------

##### Dream

| **Field Label**    | **Field Name**      | **Field gType** | **Required/Optional** |
|--------------------|---------------------|-----------------|-----------------------|
| `commentsCount`    | `comments_count`    | `int`           | Optional              |
| `createdAt`        | `created_at`        | `DateTime`      | Required              |
| `description`      | `description`       | `String`        | Optional              |
| `employmentStatus` | `employment_status` | `int`           | Optional              |
| `expert`           | `expert`            | `Object`        | Optional              |
| `finalPrice`       | `final_price`       | `num`           | Required              |
| `gender`           | `gender`            | `int`           | Optional              |
| `id`               | `id`                | `int`           | Required              |
| `isFavorite`       | `is_favorite`       | `bool`          | Required              |
| `late`             | `late`              | `bool`          | Optional              |
| `materialStatus`   | `material_status`   | `int`           | Optional              |
| `paid`             | `paid`              | `bool`          | Optional              |
| `paidDate`         | `paid_date`         | `DateTime`      | Optional              |
| `paymentMethod`    | `payment_method`    | `Object`        | Optional              |
| `price`            | `price`             | `num`           | Required              |
| `promoCode`        | `promo_code`        | `String`        | Optional              |
| `reviewDate`       | `review_date`       | `DateTime`      | Optional              |
| `reviewStars`      | `review_stars`      | `num`           | Optional              |
| `reviewText`       | `review_text`       | `String`        | Optional              |
| `status`           | `status`            | `int`           | Required              |
| `title`            | `title`             | `String`        | Optional              |
| `type`             | `type`              | `Object`        | Optional              |
| `updatedAt`        | `updated_at`        | `DateTime`      | Required              |
| `user`             | `user`              | `Object`        | Optional              |
| `views`            | `views`             | `int`           | Optional              |

### Dream Enumerations
---------------------

##### DreamEmploymentStatus

| **Field Label** | **Field Name** | 
|-----------------|----------------|
| `Student`       | `1`            |
| `Employee`      | `2`            |
| `Unemployed`    | `3`            |

##### DreamMaritalStatus

| **Field Label** | **Field Name** | 
|-----------------|----------------|
| `Single`        | `1`            |
| `Married`       | `2`            |
| `Widow`         | `3`            |
| `Divorced`      | `4`            |

##### DreamStatus

| **Field Label** | **Field Name** | 
|-----------------|----------------|
| `Pending`       | `1`            |
| `Accepted`      | `2`            |
| `Rejected`      | `3`            |
| `In Progress`   | `4`            |
| `Done`          | `5`            |
| `Cancelled`     | `6`            |
| `Draft`         | `7`            |

### Dream Parameters
---------------------

##### DreamCreationDataParameters (api/v1/dreams)

| **Field Label**           | **Field Name**               | **Field gType** | **Required/Optional** |
|---------------------------|------------------------------|-----------------|-----------------------|
| `audios`                  | `audios`                     | `Array of File` | Optional              |
| `description`             | `description`                | `String`        | Optional              |
| `dreamID`                 | `dream_id`                   | `int`           | Required              |
| `employmentStatus`        | `employment_status`          | `int`           | Optional              |
| `expertId`                | `expert_id`                  | `int`           | Optional              |
| `finalPrice`              | `final_price`                | `num`           | Optional              |
| `gender`                  | `gender`                     | `int`           | Optional              |
| `internalPaymentMethodId` | `internal_payment_method_id` | `int`           | Optional              |
| `maritalStatus`           | `marital_status`             | `int`           | Optional              |
| `paymentMethodId`         | `payment_method_id`          | `int`           | Optional              |
| `price`                   | `price`                      | `num`           | Optional              |
| `promoCode`               | `promo_code`                 | `String`        | Optional              |
| `status`                  | `status`                     | `int`           | Required              |
| `title`                   | `title`                      | `String`        | Optional              |
| `typeId`                  | `type_id`                    | `int`           | Required              |

##### ExpertDreamsParameters (api/v1/dreams/$expertId/expert)

| **Field Label** | **Field Name** | **Field gType** | **Required/Optional** |
|-----------------|----------------|-----------------|-----------------------|
| `expertId`      | `expertId`     | `int`           | Required              |
| `page`          | `page`         | `int`           | Required              |
| `limit`         | `perPage`      | `int`           | Required              |
| `sortBy`        | `sortKey`      | `String`        | Optional              |
| `sortType`      | `sortType`     | `String`        | Optional              |
| `isLate`        | `isLate`       | `bool`          | Optional              |
| `isPublic`      | `isPublic`     | `bool`          | Optional              |
| `typeId`        | `typeId`       | `int`           | Optional              |

##### DreamsParameters (api/v1/dreams)

| **Field Label** | **Field Name** | **Field gType** | **Required/Optional** |
|-----------------|----------------|-----------------|-----------------------|
| `page`          | `page`         | `int`           | Required              |
| `limit`         | `perPage`      | `int`           | Required              |
| `sortBy`        | `sortKey`      | `String`        | Optional              |
| `sortType`      | `sortType`     | `String`        | Optional              |
| `isLate`        | `isLate`       | `bool`          | Optional              |
| `isPublic`      | `isPublic`     | `bool`          | Optional              |
| `typeId`        | `typeId`       | `int`           | Optional              |

##### ReportDreamParameters (api/v1/dreams/${dreamId}/report)

| **Field Label** | **Field Name** | **Field gType** | **Required/Optional** |
|-----------------|----------------|-----------------|-----------------------|
| `dreamId`       | `id`           | `int`           | Optional              |
| `message`       | `message`      | `String`        | Optional              |

##### DreamModificationDataParameters (api/v1/dreams/${userId}/user)

| **Field Label**    | **Field Name**      | **Field gType** | **Required/Optional** |
|--------------------|---------------------|-----------------|-----------------------|
| `audios`           | `audios`            | `Array of File` | Optional              |
| `description`      | `description`       | `String`        | Optional              |
| `dreamID`          | `dream_id`          | `int`           | Optional              |
| `employmentStatus` | `employment_status` | `int`           | Optional              |
| `expertId`         | `expert_id`         | `int`           | Optional              |
| `finalPrice`       | `final_price`       | `num`           | Optional              |
| `gender`           | `gender`            | `int`           | Optional              |
| `maritalStatus`    | `marital_status`    | `int`           | Optional              |
| `paymentMethodId`  | `payment_method_id` | `int`           | Optional              |
| `price`            | `price`             | `num`           | Optional              |
| `title`            | `title`             | `String`        | Optional              |
| `typeId`           | `type_id`           | `int`           | Optional              |

##### UserDreamsParameters (api/v1/dreams/${userId}/user)

| **Field Label** | **Field Name** | **Field gType** | **Required/Optional** |
|-----------------|----------------|-----------------|-----------------------|
| `userId`        | `userId`       | `int`           | Required              |
| `page`          | `page`         | `int`           | Required              |
| `limit`         | `perPage`      | `int`           | Required              |
| `sortBy`        | `sortKey`      | `String`        | Optional              |
| `sortType`      | `sortType`     | `String`        | Optional              |
| `status`        | `status`       | `int`           | Optional              |
| `isPublic`      | `isPublic`     | `bool`          | Optional              |
| `typeId`        | `typeId`       | `int`           | Optional              |

## DreamInterpreter
---------------------

### DreamInterpreter Entity
---------------------

##### DreamInterpreter

| **Field Label**  | **Field Name**   | **Field Type** | **Required/Optional** |
|------------------|------------------|----------------|-----------------------|
| `achievedDreams` | `achived_dreams` | `int`          | Required              |
| `bio`            | `bio`            | `String`       | Optional              |
| `deletedAt`      | `deleted_at`     | `DateTime`     | Optional              |
| `email`          | `email`          | `String`       | Required              |
| `firstName`      | `first_name`     | `String`       | Required              |
| `fullName`       | `full_name`      | `String`       | Required              |
| `id`             | `id`             | `int`          | Required              |
| `image`          | `image`          | `String`       | Optional              |
| `lastName`       | `last_name`      | `String`       | Required              |
| `phone`          | `phone`          | `String`       | Required              |
| `rating`         | `rating`         | `num`          | Required              |
| `waitingDreams`  | `waiting_dreams` | `int`          | Required              |

### DreamInterpreter Parameters
---------------------

##### DreamInterpretersParameters (api/v1/experts)

| **Field Label**   | **Field Name** | **Field gType** | **Required/Optional** |
|-------------------|----------------|-----------------|-----------------------|
| `interpreterName` | `query`        | `String`        | Optional              |
| `page`            | `page`         | `int`           | Required              |
| `limit`           | `perPage`      | `int`           | Required              |

## DreamReview
---------------------

### DreamReview Entity
---------------------

##### DreamReview

| **Field Label** | **Field Name** | **Field Type** | **Required/Optional** |
|-----------------|----------------|----------------|-----------------------|
| `date`          | `review_date`  | `DateTime`     | Optional              |
| `stars`         | `review_stars` | `num`          | Optional              |
| `text`          | `review_text`  | `String`       | Optional              |
| `user`          | `user`         | `User Object`  | Required              |

### DreamReview Parameters
---------------------

##### CreateDreamReviewParameters (api/v1/dreams/$id/review)

| **Field Label** | **Field Name** | **Field gType** | **Required/Optional** |
|-----------------|----------------|-----------------|-----------------------|
| `id`            | `id`           | `int`           | Required              |
| `stars`         | `stars`        | `review_stars`  | Required              |
| `text`          | `text`         | `review_text`   | Required              |

##### DreamReviewsParameters (api/v1/reviews/$id)

| **Field Label** | **Field Name** | **Field gType** | **Required/Optional** |
|-----------------|----------------|-----------------|-----------------------|
| `interpreterId` | `id`           | `int`           | Required              |
| `page`          | `page`         | `int`           | Required              |
| `limit`         | `perPage`      | `int`           | Required              |
| `sortBy`        | `sortKey`      | `String`        | Optional              |
| `sortType`      | `sortType`     | `String`        | Optional              |

## DreamType
---------------------

### DreamType Entity
---------------------

##### DreamType

| **Field Label**          | **Field Name**              | **Field Type**           | **Required/Optional** |
|--------------------------|-----------------------------|--------------------------|-----------------------|
| `active`                 | `active`                    | `bool`                   | Required              |
| `audioLimit`             | `audio_limit`               | `num`                    | Optional              |
| `createdAt`              | `created_at`                | `DateTime`               | Required              |
| `flag`                   | `special_flag`              | `String`                 | Optional              |
| `id`                     | `id`                        | `int`                    | Required              |
| `lettersLimit`           | `letters_limit`             | `int`                    | Optional              |
| `name`                   | `name`                      | `String`                 | Required              |
| `notes`                  | `notes`                     | `Array of DreamTypeNote` | Required              |
| `price`                  | `price`                     | `num`                    | Required              |
| `public`                 | `public`                    | `bool`                   | Required              |
| `waitingForApproveTime`  | `waiting_for_approve_time`  | `num`                    | Optional              |
| `waitingForResponseTime` | `waiting_for_response_time` | `num`                    | Optional              |

##### DreamTypeNote

| **Field Label** | **Field Name** | **Field Type** | **Required/Optional** |
|-----------------|----------------|----------------|-----------------------|
| `id`            | `id`           | `int`          | Required              |
| `text`          | `text`         | `String`       | Required              |

### DreamType Parameters
---------------------

##### DreamTypesParameters (api/v1/dreams/types)

| **Field Label** | **Field Name** | **Field gType** | **Required/Optional** |
|-----------------|----------------|-----------------|-----------------------|
| `isActive`      | `isActive`     | `int`           | Required              |
| `page`          | `page`         | `int`           | Required              |
| `limit`         | `perPage`      | `int`           | Required              |

## Favourite
---------------------

### Favourite Parameters
---------------------

##### FavouritesParameters (api/v1/favorites)

| **Field Label** | **Field Name** | **Field gType** | **Required/Optional** |
|-----------------|----------------|-----------------|-----------------------|
| `page`          | `page`         | `int`           | Required              |
| `limit`         | `perPage`      | `int`           | Required              |
| `sortBy`        | `sortKey`      | `String`        | Optional              |
| `sortType`      | `sortType`     | `String`        | Optional              |

## Home
---------------------

### Home Parameters
---------------------

##### HomeDataParameters (api/v1/home)

| **Field Label** | **Field Name** | **Field gType** | **Required/Optional** |
|-----------------|----------------|-----------------|-----------------------|
| `page`          | `page`         | `int`           | Required              |
| `limit`         | `perPage`      | `int`           | Required              |
| `sortBy`        | `sortKey`      | `String`        | Optional              |
| `sortType`      | `sortType`     | `String`        | Optional              |

## Notification
---------------------

### Notification Entity
---------------------

##### Notification

| **Field Label** | **Field Name** | **Field Type** | **Required/Optional** |
|-----------------|----------------|----------------|-----------------------|
| `body`          | `body`         | `String`       | Required              |
| `createdAt`     | `created_at`   | `DateTime`     | Required              |
| `id`            | `id`           | `int`          | Required              |
| `image`         | `image`        | `String`       | Optional              |
| `sender`        | `sender`       | `User Object`  | Optional              |
| `target`        | `target`       | `int`          | Optional              |
| `targetType`    | `target_type`  | `int`          | Optional              |
| `title`         | `title`        | `String`       | Required              |

### Notification Parameters
---------------------

##### NotificationsParameters (api/v1/user/notifications)

| **Field Label** | **Field Name** | **Field gType** | **Required/Optional** |
|-----------------|----------------|-----------------|-----------------------|
| `page`          | `page`         | `int`           | Required              |
| `limit`         | `perPage`      | `int`           | Required              |
| `sortBy`        | `sortKey`      | `String`        | Optional              |
| `sortType`      | `sortType`     | `String`        | Optional              |

## Package
---------------------

### Package Entity
---------------------

##### Package

| **Field Label** | **Field Name** | **Field gType** | **Required/Optional** |
|-----------------|----------------|-----------------|-----------------------|
| `balance`       | `balance`      | `num`           | Required              |
| `createdAt`     | `created_at`   | `DateTime`      | Required              |
| `description`   | `description`  | `String`        | Required              |
| `discount`      | `discount`     | `num`           | Required              |
| `id`            | `id`           | `int`           | Required              |
| `name`          | `name`         | `String`        | Optional              |
| `price`         | `price`        | `num`           | Required              |
| `updatedAt`     | `updated_at`   | `DateTime`      | Optional              |

##### PackageSubscription

| **Field Label** | **Field Name**   | **Field gType**             | **Required/Optional** |
|-----------------|------------------|-----------------------------|-----------------------|
| `amount`        | `amount`         | `num`                       | Required              |
| `id`            | `id`             | `int`                       | Required              |
| `package`       | `package`        | `Package`                   | Optional              |
| `paymentMethod` | `payment_method` | `PaymentMethod`             | Required              |
| `status`        | `status`         | `PackageSubscriptionStatus` | Required              |
| `transaction`   | `transaction`    | `UserTransaction`           | Optional              |
| `user`          | `user`           | `UserDetails`               | Required              |

### Package Enumerations
---------------------

##### PackageSubscriptionStatus

| **Field Label** | **Field Name** | 
|-----------------|----------------|
| `Unpaid`        | `0`            |
| `Paid`          | `1`            |

### Package Parameters
---------------------

##### PackageSubscribeParameters (api/v1/package/subscribe)

| **Field Label**           | **Field Name**               | **Field gType** | **Required/Optional** |
|---------------------------|------------------------------|-----------------|-----------------------|
| `amount`                  | `amount`                     | `num`           | Optional              |
| `internalPaymentMethodId` | `internal_payment_method_id` | `int`           | Optional              |
| `packageIds`              | `package_ids`                | `Array of int`  | Optional              |
| `paymentMethodId`         | `payment_method_id`          | `int`           | Required              |

##### PackagesParameters (api/v1/packages)

| **Field Label** | **Field Name** | **Field gType** | **Required/Optional** |
|-----------------|----------------|-----------------|-----------------------|
| `active`        | `active`       | `bool`          | Optional              |
| `page`          | `page`         | `int`           | Required              |
| `limit`         | `perPage`      | `int`           | Required              |
| `sortBy`        | `sortKey`      | `String`        | Optional              |
| `sortType`      | `sortType`     | `String`        | Optional              |

##### SubscriptionsPackagesParameters (api/v1/subscriptions)

| **Field Label** | **Field Name** | **Field gType** | **Required/Optional** |
|-----------------|----------------|-----------------|-----------------------|
| `active`        | `active`       | `bool`          | Optional              |
| `page`          | `page`         | `int`           | Required              |
| `limit`         | `perPage`      | `int`           | Required              |
| `sortBy`        | `sortKey`      | `String`        | Optional              |
| `sortType`      | `sortType`     | `String`        | Optional              |

## PaymentMethod
---------------------

### PaymentMethod Entity
---------------------

##### PaymentMethod

| **Field Label** | **Field Name** | **Field gType** | **Required/Optional** |
|-----------------|----------------|-----------------|-----------------------|
| `id`            | `id`           | `int`           | Required              |
| `image`         | `image`        | `String`        | Optional              |
| `name`          | `name`         | `String`        | Required              |
| `online`        | `online`       | `bool`          | Required              |

##### InternalPaymentMethod

| **Field Label**       | **Field Name**        | **Field gType** | **Required/Optional** |
|-----------------------|-----------------------|-----------------|-----------------------|
| `currencyIso`         | `currencyIso`         | `String`        | Required              |
| `imageUrl`            | `imageUrl`            | `String`        | Required              |
| `isDirectPayment`     | `isDirectPayment`     | `bool`          | Required              |
| `isEmbeddedSupported` | `isEmbeddedSupported` | `bool`          | Required              |
| `paymentCurrencyIso`  | `paymentCurrencyIso`  | `String`        | Required              |
| `paymentMethodAr`     | `paymentMethodAr`     | `String`        | Required              |
| `paymentMethodCode`   | `paymentMethodCode`   | `String`        | Required              |
| `paymentMethodEn`     | `paymentMethodEn`     | `String`        | Required              |
| `paymentMethodId`     | `paymentMethodId`     | `int`           | Required              |
| `serviceCharge`       | `serviceCharge`       | `num`           | Required              |
| `totalAmount`         | `totalAmount`         | `num`           | Required              |

### PaymentMethod Parameters
---------------------

##### PaymentMethodsParameters (api/v1/payment-methods)

| **Field Label** | **Field Name** | **Field gType** | **Required/Optional** |
|-----------------|----------------|-----------------|-----------------------|
| `page`          | `page`         | `int`           | Required              |
| `limit`         | `perPage`      | `int`           | Required              |

##### InternalPaymentMethodsParameters (api/v1/internal-payment-methods/$paymentMethodId)

| **Field Label**   | **Field Name**    | **Field gType** | **Required/Optional** |
|-------------------|-------------------|-----------------|-----------------------|
| `page`            | `page`            | `int`           | Required              |
| `limit`           | `perPage`         | `int`           | Required              |
| `paymentMethodId` | `paymentMethodId` | `int`           | Required              |

## PromoCode
---------------------

### PromoCode Entity
---------------------

##### PromoCode

| **Field Label**      | **Field Name**       | **Field gType** | **Required/Optional** |
|----------------------|----------------------|-----------------|-----------------------|
| `finalPrice`         | `finalPrice`         | `num`           | Required              |
| `price`              | `price`              | `num`           | Required              |
| `promoDiscountPrice` | `promoDiscountPrice` | `num`           | Required              |

### PromoCode Enumerations
---------------------

##### PromoCodeUserType

| **Field Label** | **Field Name** | 
|-----------------|----------------|
| `All`           | `1`            |
| `Selection`     | `2`            |

##### PromoCodeType

| **Field Label** | **Field Name** | 
|-----------------|----------------|
| `Fixed Amount`  | `1`            |
| `Percentage`    | `2`            |

##### PromoCodeUsageType

| **Field Label** | **Field Name** | 
|-----------------|----------------|
| `One Time Use`  | `1`            |
| `Daily Use`     | `2`            |
| `Unlimited Use` | `3`            |

### PromoCode Parameters
---------------------

##### CheckPromoCodeParameters (api/v1/check-promo-code)

| **Field Label** | **Field Name** | **Field gType** | **Required/Optional** |
|-----------------|----------------|-----------------|-----------------------|
| `price`         | `price`        | `num`           | Required              |
| `promoCode`     | `promo_code`   | `String`        | Required              |

## User
---------------------

### User Entity
---------------------

##### User

| **Field Label** | **Field Name** | **Field gType** | **Required/Optional** |
|-----------------|----------------|-----------------|-----------------------|
| `accessToken`   | `access_token` | `String`        | Required              |
| `detials`       | `user_details` | `UserDetails`   | Required              |

##### UserDetails

| **Field Label**       | **Field Name**         | **Field gType** | **Required/Optional** |
|-----------------------|------------------------|-----------------|-----------------------|
| `bio`                 | `bio`                  | `String`        | Optional              |
| `birthday`            | `birthday`             | `DateTime`      | Optional              |
| `chatId`              | `chat_id`              | `int`           | Required              |
| `commissionType`      | `commission_type`      | `int`           | Required              |
| `commissionValue`     | `commission_value`     | `num`           | Required              |
| `createdAt`           | `created_at`           | `DateTime`      | Required              |
| `deletedAt`           | `deleted_at`           | `DateTime`      | Optional              |
| `email`               | `email`                | `String`        | Required              |
| `emailVerified`       | `email_verified`       | `bool`          | Required              |
| `employmentStatus`    | `employment_status`    | `int`           | Optional              |
| `firstName`           | `first_name`           | `String`        | Optional              |
| `fullName`            | `full_name`            | `String`        | Optional              |
| `gender`              | `gender`               | `int`           | Required              |
| `id`                  | `id`                   | `int`           | Required              |
| `image`               | `image`                | `String`        | Optional              |
| `imageId`             | `image_id`             | `int`           | Optional              |
| `isBusy`              | `is_busy`              | `bool`          | Required              |
| `isOnline`            | `is_online`            | `bool`          | Required              |
| `lastName`            | `last_name`            | `String`        | Optional              |
| `maritalStatus`       | `marital_status`       | `int`           | Optional              |
| `notificationEnabled` | `notification_enabled` | `bool`          | Required              |
| `phone`               | `phone`                | `String`        | Required              |
| `phoneVerified`       | `phone_verified`       | `bool`          | Required              |
| `role`                | `role_id`              | `int`           | Required              |
| `updatedAt`           | `updated_at`           | `DateTime`      | Required              |
| `wallet`              | `wallet`               | `num`           | Required              |

### User Enumerations
---------------------

##### CommissionType

| **Field Label** | **Field Name** | 
|-----------------|----------------|
| `Fixed`         | `fixed`        |
| `Percentage`    | `percentage`   |

##### EmploymentStatus

| **Field Label** | **Field Name** | 
|-----------------|----------------|
| `Student`       | `1`            |
| `Employee`      | `2`            |
| `Unemployed`    | `3`            |

##### MaritalStatus

| **Field Label** | **Field Name** | 
|-----------------|----------------|
| `Single`        | `1`            |
| `Married`       | `2`            |
| `Widow`         | `3`            |
| `Divorced`      | `4`            |

### User Parameters
---------------------

##### AddFcmTokenParameters (api/v1/add_push_message_token)

| **Field Label** | **Field Name** | **Field gType** | **Required/Optional** |
|-----------------|----------------|-----------------|-----------------------|
| `platform`      | `platform`     | `String`        | Required              |
| `token`         | `token`        | `String`        | Required              |

##### ReadUserParameters (api/v1/users/$userId)

| **Field Label** | **Field Name** | **Field gType** | **Required/Optional** |
|-----------------|----------------|-----------------|-----------------------|
| `userId`        | `id`           | `int`           | Required              |

##### ToggleNotificationParameters (api/v1/users/$userId/toggle-notifications)

| **Field Label**       | **Field Name**         | **Field gType** | **Required/Optional** |
|-----------------------|------------------------|-----------------|-----------------------|
| `notificationEnabled` | `notification_enabled` | `bool`          | Required              |
| `userId`              | `user_id`              | `int`           | Required              |

##### UserToggleOnlineParameters (api/v1/users/toggle-online)

| **Field Label** | **Field Name** | **Field gType** | **Required/Optional** |
|-----------------|----------------|-----------------|-----------------------|
| `isOnline`      | `is_online`    | `bool`          | Required              |
| `platform`      | `platform`     | `String`        | Required              |

##### VerifyAccountParameters (api/v1/verify-phone)

| **Field Label** | **Field Name** | **Field gType** | **Required/Optional** |
|-----------------|----------------|-----------------|-----------------------|
| `otp`           | `otp`          | `String`        | Required              |

## UserTransaction
---------------------

### UserTransaction Entity
---------------------

##### UserTransaction

| **Field Label** | **Field Name** | **Field gType** | **Required/Optional** |
|-----------------|----------------|-----------------|-----------------------|
| `amount`        | `amount`       | `String`        | Required              |
| `createdAt`     | `created_at`   | `DateTime`      | Required              |
| `id`            | `id`           | `int`           | Required              |
| `method`        | `method`       | `PaymentMethod` | Optional              |
| `name`          | `name`         | `String`        | Required              |
| `paid`          | `paid`         | `bool`          | Required              |
| `payableId`     | `payable_id`   | `int`           | Required              |
| `payableType`   | `payable_type` | `String`        | Required              |
| `userId`        | `user_id`      | `int`           | Required              |
| `user`          | `user`         | `UserDetails`   | Required              |

### UserTransaction Parameters
---------------------

##### MyTransactionsParameters (api/v1/user-transactions)

| **Field Label** | **Field Name** | **Field gType** | **Required/Optional** |
|-----------------|----------------|-----------------|-----------------------|
| `page`          | `page`         | `int`           | Required              |
| `limit`         | `perPage`      | `int`           | Required              |
