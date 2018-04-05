---
UID: NF:wuapi.IAutomaticUpdatesSettings2.CheckPermission
title: IAutomaticUpdatesSettings2::CheckPermission method
author: windows-driver-content
description: Determines whether a specific user or type of user has permission to perform a selected action.
old-location: wua\iautomaticupdatessettings2_checkpermission.htm
old-project: Wua_Sdk
ms.assetid: fbf36d9f-98c1-4b9d-b479-a9203b6ce952
ms.author: windowsdriverdev
ms.date: 3/15/2018
ms.keywords: CheckPermission method [Windows Update Agent], CheckPermission method [Windows Update Agent], IAutomaticUpdatesSettings2 interface, CheckPermission,IAutomaticUpdatesSettings2.CheckPermission, IAutomaticUpdatesSettings2, IAutomaticUpdatesSettings2 interface [Windows Update Agent], CheckPermission method, IAutomaticUpdatesSettings2::CheckPermission, wua.iautomaticupdatessettings2_checkpermission, wuapi/IAutomaticUpdatesSettings2::CheckPermission
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: UpdateType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wuapi.dll
api_name:
-	IAutomaticUpdatesSettings2.CheckPermission
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IAutomaticUpdatesSettings2::CheckPermission method


## -description


<p class="CCE_Message">[<b>IAutomaticUpdatesSettings2::CheckPermission</b> is no longer supported. Starting with 
    Windows 10 calls to <b>CheckPermission</b> always return <b>S_OK</b>, and a return value of <b>VARIANT_TRUE</b> (users have permissions). However, <b>IAutomaticUpdatesSettings::Save</b> is a no-op, so no changes can be made.]


Determines whether a specific user or type of user has permission to perform a selected action.




## -parameters




### -param userType




### -param permissionType




### -param userHasPermission






#### - AutomaticUpdatesPermissionType [in]

An enumeration that indicates the user's permission level.


#### - AutomaticUpdatesUserType [in]

An enumeration that indicates the type of user to verify permissions.


## -returns



Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code.




## -remarks



This method can be used to determine whether User Access Control (UAC) must be used to perform an action in the agent, which may obviate the need for prompting if the user type does not have permission to perform the action.  For example, unless the agent has elevated permission, the <a href="https://msdn.microsoft.com/e7a066b9-9581-4573-82e2-a6f2ca7440ac">ReadOnly</a> property of the <a href="https://msdn.microsoft.com/c4672df5-9e47-45f5-9504-1ebb0bf3c6a6">IAutomaticUpdatesSettings</a> interface will always be <b>VARIANT_TRUE</b>.  However, even after a user has been elevated, the <a href="https://msdn.microsoft.com/a326400b-d6df-4947-8ab8-126d357834c3">NotificationLevel</a> (for example) may still be read-only due to Group Policy settings.  The <b>CheckPermission</b> method can determine this before elevation is done to prevent prompting in cases where the setting cannot be changed.




## -see-also




<a href="https://msdn.microsoft.com/5ad1a3ee-3293-4825-a85e-ca1e3a38e775">IAutomaticUpdatesSettings2</a>
 

 

