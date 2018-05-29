---
UID: NF:cscobj.IOfflineFilesSetting.DeletePreference
title: IOfflineFilesSetting::DeletePreference
author: windows-sdk-content
description: Removes a preference setting.
old-location: of\iofflinefilessetting_deletepreference.htm
old-project: OfflineFiles
ms.assetid: 815791e8-3e41-4511-9789-9b9258e5fcf4
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: DeletePreference, DeletePreference method [Offline Files], DeletePreference method [Offline Files],IOfflineFilesSetting interface, IOfflineFilesSetting interface [Offline Files],DeletePreference method, IOfflineFilesSetting.DeletePreference, IOfflineFilesSetting::DeletePreference, OFFLINEFILES_SETTING_SCOPE_COMPUTER, OFFLINEFILES_SETTING_SCOPE_USER, cscobj/IOfflineFilesSetting::DeletePreference, of.iofflinefilessetting_deletepreference
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: cscobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: OFFLINEFILES_SYNC_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CscSvc.dll
-	CscObj.dll
api_name:
-	IOfflineFilesSetting.DeletePreference
product: Windows
targetos: Windows
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
---

# IOfflineFilesSetting::DeletePreference


## -description


Removes a preference setting.


## -parameters




### -param dwScope [in]

Indicates which preference setting is to be deleted.  Must be one of the following.



#### OFFLINEFILES_SETTING_SCOPE_USER (0x00000001)

The user preference setting is to be deleted.



#### OFFLINEFILES_SETTING_SCOPE_COMPUTER (0x00000002)

The machine preference setting is to be deleted.


## -returns



<b>S_OK</b> if the preference is removed successfully or an error value otherwise.

Returns <code>HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)</code> if the requested preference setting is not currently configured.

Returns <code>HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)</code> if the caller is trying to remove a per-machine preference and is not a local administrator.




## -remarks



This method requires system administrator privilege if the preference is a per-machine preference.




## -see-also




<a href="https://msdn.microsoft.com/6f47c67b-9438-4229-89b2-6b3f9da8fb68">IOfflineFilesSetting</a>
 

 

