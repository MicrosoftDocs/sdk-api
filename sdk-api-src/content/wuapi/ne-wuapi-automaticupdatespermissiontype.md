---
UID: NE:wuapi.tagAutomaticUpdatesPermissionType
title: AutomaticUpdatesPermissionType (wuapi.h)
description: Defines the possible ways to set the NotificationLevel property of the IAutomaticUpdatesSettings interface or the IncludeRecommendedUpdates property of the IAutomaticUpdatesSettings2 interface.
helpviewer_keywords: ["AutomaticUpdatesPermissionType","AutomaticUpdatesPermissionType enumeration [Windows Update Agent]","auptDisableAutomaticUpdates","auptSetFeaturedUpdatesEnabled","auptSetIncludeRecommendedUpdates","auptSetNonAdministratorsElevated","auptSetNotificationLevel","wua.automaticupdatespermissiontype","wuapi/AutomaticUpdatesPermissionType","wuapi/auptDisableAutomaticUpdates","wuapi/auptSetFeaturedUpdatesEnabled","wuapi/auptSetIncludeRecommendedUpdates","wuapi/auptSetNonAdministratorsElevated","wuapi/auptSetNotificationLevel"]
old-location: wua\automaticupdatespermissiontype.htm
tech.root: wua
ms.assetid: 0bacce1d-438d-4d33-91f8-235ffe26abb2
ms.date: 12/05/2018
ms.keywords: AutomaticUpdatesPermissionType, AutomaticUpdatesPermissionType enumeration [Windows Update Agent], auptDisableAutomaticUpdates, auptSetFeaturedUpdatesEnabled, auptSetIncludeRecommendedUpdates, auptSetNonAdministratorsElevated, auptSetNotificationLevel, wua.automaticupdatespermissiontype, wuapi/AutomaticUpdatesPermissionType, wuapi/auptDisableAutomaticUpdates, wuapi/auptSetFeaturedUpdatesEnabled, wuapi/auptSetIncludeRecommendedUpdates, wuapi/auptSetNonAdministratorsElevated, wuapi/auptSetNotificationLevel
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: AutomaticUpdatesPermissionType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagAutomaticUpdatesPermissionType
 - wuapi/tagAutomaticUpdatesPermissionType
 - AutomaticUpdatesPermissionType
 - wuapi/AutomaticUpdatesPermissionType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wuapi.h
api_name:
 - AutomaticUpdatesPermissionType
---

# AutomaticUpdatesPermissionType enumeration


## -description

Defines the possible ways to set the <a href="/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel">NotificationLevel</a> property of the <a href="/windows/desktop/api/wuapi/nn-wuapi-iautomaticupdatessettings">IAutomaticUpdatesSettings</a> interface or the <a href="/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdatessettings2-get_includerecommendedupdates">IncludeRecommendedUpdates</a> property of the <a href="/windows/desktop/api/wuapi/nn-wuapi-iautomaticupdatessettings2">IAutomaticUpdatesSettings2</a> interface.

## -enum-fields

### -field auptSetNotificationLevel:1

The ability to set the <a href="/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel">IAutomaticUpdatesSettings::NotificationLevel</a> property.

### -field auptDisableAutomaticUpdates:2

The ability to set the <a href="/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel">IAutomaticUpdatesSettings::NotificationLevel</a> property to <a href="/windows/desktop/api/wuapi/ne-wuapi-automaticupdatesnotificationlevel">aunlDisabled</a>.

### -field auptSetIncludeRecommendedUpdates:3

The ability to set the <a href="/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdatessettings2-get_includerecommendedupdates">IAutomaticUpdatesSettings2::IncludedRecommendedUpdates</a> property.

### -field auptSetFeaturedUpdatesEnabled:4

The ability to set the <a href="/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdatessettings3-get_featuredupdatesenabled">IAutomaticUpdatesSettings3::FeaturedUpdatesEnabled</a> property.

### -field auptSetNonAdministratorsElevated:5

The ability to set the <a href="/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdatessettings3-get_nonadministratorselevated">IAutomaticUpdatesSettings3::NonAdministratorsElevated</a> property.

## -remarks

Featured update notifications are only supported on Windows Vista and above. On Windows XP systems running versions of the Windows Update Agent (WUA) that support <a href="/windows/desktop/api/wuapi/nn-wuapi-iautomaticupdatessettings3">IAutomaticUpdatesSettings3</a>, the <a href="/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdatessettings3-get_featuredupdatesenabled">IAutomaticUpdatesSettings3::FeaturedUpdatesEnabled</a> value will always be VARIANT_FALSE, and attempting to alter its value will result in an error.

Featured update notifications are only supported when Automatic Updates is turned on. If Automatic Updates is set to “Never check for updates (not recommended),” then the <a href="/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdatessettings3-get_featuredupdatesenabled">IAutomaticUpdatesSettings3::FeaturedUpdatesEnabled</a> value will always be VARIANT_FALSE, and attempting to alter its value will result in an error.

Featured update notifications are only supported on certain update services. Currently, the only supported update service is Microsoft Update. If Automatic Updates is currently configured to receive updates from another service (from Windows Update, or from a WSUS server), then  the <a href="/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdatessettings3-get_featuredupdatesenabled">IAutomaticUpdatesSettings3::FeaturedUpdatesEnabled</a> value will always be VARIANT_FALSE, and attempting to alter its value will result in an error.
