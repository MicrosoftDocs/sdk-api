---
UID: NF:wuapi.IAutomaticUpdatesSettings2.CheckPermission
title: IAutomaticUpdatesSettings2::CheckPermission (wuapi.h)
description: Determines whether a specific user or type of user has permission to perform a selected action.
helpviewer_keywords: ["CheckPermission","CheckPermission method [Windows Update Agent]","CheckPermission method [Windows Update Agent]","IAutomaticUpdatesSettings2 interface","IAutomaticUpdatesSettings2 interface [Windows Update Agent]","CheckPermission method","IAutomaticUpdatesSettings2.CheckPermission","IAutomaticUpdatesSettings2::CheckPermission","wua.iautomaticupdatessettings2_checkpermission","wuapi/IAutomaticUpdatesSettings2::CheckPermission"]
old-location: wua\iautomaticupdatessettings2_checkpermission.htm
tech.root: wua
ms.assetid: fbf36d9f-98c1-4b9d-b479-a9203b6ce952
ms.date: 12/05/2018
ms.keywords: CheckPermission, CheckPermission method [Windows Update Agent], CheckPermission method [Windows Update Agent],IAutomaticUpdatesSettings2 interface, IAutomaticUpdatesSettings2 interface [Windows Update Agent],CheckPermission method, IAutomaticUpdatesSettings2.CheckPermission, IAutomaticUpdatesSettings2::CheckPermission, wua.iautomaticupdatessettings2_checkpermission, wuapi/IAutomaticUpdatesSettings2::CheckPermission
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
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAutomaticUpdatesSettings2::CheckPermission
 - wuapi/IAutomaticUpdatesSettings2::CheckPermission
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IAutomaticUpdatesSettings2.CheckPermission
---

# IAutomaticUpdatesSettings2::CheckPermission


## -description

<p class="CCE_Message">[<b>IAutomaticUpdatesSettings2::CheckPermission</b> is no longer supported. Starting with 
    Windows 10 calls to <b>CheckPermission</b> always return <b>S_OK</b>, and a return value of <b>VARIANT_TRUE</b> (users have permissions). However, <b>IAutomaticUpdatesSettings::Save</b> is a no-op, so no changes can be made.]


Determines whether a specific user or type of user has permission to perform a selected action.

## -parameters

### -param userType [in]

An enumeration that indicates the type of user to verify permissions.

### -param permissionType [in]

An enumeration that indicates the user's permission level.

### -param userHasPermission

True if the user has the specified permission type; otherwise, false.

## -returns

Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code.

## -remarks

This method can be used to determine whether User Access Control (UAC) must be used to perform an action in the agent, which may obviate the need for prompting if the user type does not have permission to perform the action.  For example, unless the agent has elevated permission, the <a href="/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdatessettings-get_readonly">ReadOnly</a> property of the <a href="/windows/desktop/api/wuapi/nn-wuapi-iautomaticupdatessettings">IAutomaticUpdatesSettings</a> interface will always be <b>VARIANT_TRUE</b>.  However, even after a user has been elevated, the <a href="/windows/desktop/api/wuapi/ne-wuapi-automaticupdatesnotificationlevel">NotificationLevel</a> (for example) may still be read-only due to Group Policy settings.  The <b>CheckPermission</b> method can determine this before elevation is done to prevent prompting in cases where the setting cannot be changed.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iautomaticupdatessettings2">IAutomaticUpdatesSettings2</a>