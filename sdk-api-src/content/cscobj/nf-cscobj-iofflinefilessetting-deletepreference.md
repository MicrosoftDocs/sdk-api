---
UID: NF:cscobj.IOfflineFilesSetting.DeletePreference
title: IOfflineFilesSetting::DeletePreference (cscobj.h)
description: Removes a preference setting.
helpviewer_keywords: ["DeletePreference","DeletePreference method [Offline Files]","DeletePreference method [Offline Files]","IOfflineFilesSetting interface","IOfflineFilesSetting interface [Offline Files]","DeletePreference method","IOfflineFilesSetting.DeletePreference","IOfflineFilesSetting::DeletePreference","OFFLINEFILES_SETTING_SCOPE_COMPUTER","OFFLINEFILES_SETTING_SCOPE_USER","cscobj/IOfflineFilesSetting::DeletePreference","of.iofflinefilessetting_deletepreference"]
old-location: of\iofflinefilessetting_deletepreference.htm
tech.root: of
ms.assetid: 815791e8-3e41-4511-9789-9b9258e5fcf4
ms.date: 12/05/2018
ms.keywords: DeletePreference, DeletePreference method [Offline Files], DeletePreference method [Offline Files],IOfflineFilesSetting interface, IOfflineFilesSetting interface [Offline Files],DeletePreference method, IOfflineFilesSetting.DeletePreference, IOfflineFilesSetting::DeletePreference, OFFLINEFILES_SETTING_SCOPE_COMPUTER, OFFLINEFILES_SETTING_SCOPE_USER, cscobj/IOfflineFilesSetting::DeletePreference, of.iofflinefilessetting_deletepreference
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
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOfflineFilesSetting::DeletePreference
 - cscobj/IOfflineFilesSetting::DeletePreference
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IOfflineFilesSetting.DeletePreference
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

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilessetting">IOfflineFilesSetting</a>