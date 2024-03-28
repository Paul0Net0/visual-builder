---
title: Deprecate or delete a version
order: 5
layout: post-toc
redirect_from: 
---

# Deprecate or delete a version

Deprecation is an optional process that allows you to set a date from which a non-public version of your integration will no longer be updated. Deprecation is only recommended if the older integration version will eventually stop working, such as if the related API will be removed. Zapier is normally a “set it and forget it” experience for users, so use this feature carefully. Only if the older version will no longer function, should it be deprecated. Please note that deprecating a version is significantly more disruptive to our mutual users than migrating to the latest promoted version, or than leaving users on an older (now) private version if migration is not possible.

When users are left on an older private version, they will see a [prompt in the Zap editor](https://help.zapier.com/hc/en-us/articles/18755649454989-Update-to-the-latest-app-version-in-Zaps) to optionally encourage them to make the update, instead of any deprecation communications or Zap disruptions. 

## What happens after setting a version to deprecate

### 1. Email notification

After setting the date, an initial email will be sent to users, informing them that they need to manually update their Zaps to continue using the new version. Zapier recommends supplementing these automated messages by also notifying your general user base through in-app announcements or email marketing campaigns. For privacy reasons, Zapier cannot provide you with an email list of users of your integration.

### 2. Deprecation date reached

  - Zaps that haven't been updated will be automatically paused.
  - A second email, titled “X Zaps paused over deprecated apps,” will be sent out to those users. Customizing this email is not possible.
  - The deprecated version will be labelled as “Deprecated” in the Zap editor, with a prompt for users to update to the latest version.

### 3. Post-deprecation

After the deprecation date, the version will still be visible in the Versions page for your future reference. Users will not be able to see the version once they select a different version in their Zaps. Although you can technically still invite users to the deprecated version, it's not recommended.


## Deprecate a version with Platform UI

To deprecate an integration version:

1. Log into the [Platform UI](https://zapier.com/app/developer).
2. Select your **integration**. 
3. In the _Manage_ section in the left sidebar, click **Version**. 
4. Click the **three dot** icon in line with the integration version you want to deprecate.
5. Click **Deprecate**.
6. In the dialog box, add the **Deprecate Date**. You can set a deprecation date anytime between 2 weeks and 1 year from the current date.
7. Click **Deprecate**. 
8. Click **Close**

## Deprecate a version with Platform CLI

To deprecate an integration version use the command `zapier deprecate`. Learn more about [Platform CLI commands](https://github.com/zapier/zapier-platform/blob/main/packages/cli/docs/cli.md#deprecate).

## Deleting deprecated versions

You have the option to delete versions entirely, but exercise this option with extreme caution. Deleting a version makes it permanently inaccessible, both to you and to your users. Deleted versions cannot be restored by Zapier Developer Support. 

In most scenarios, it’s advisable either to deprecate the version or leave it as a private version. Deletion should be a last resort, used only when you are certain that the version will never be needed again. 

Deletion is also only possible when 0 users remain on a version. The count of users on the _Versions_ page includes live Zaps only. If you're seeing the error `Unable to delete app version`, this can be caused by users on that version not included in the visible count (paused Zaps, app authentications for example).

![image](https://cdn.zappy.app/1722db1a2658ec77e47f5d4de58720ff.png)