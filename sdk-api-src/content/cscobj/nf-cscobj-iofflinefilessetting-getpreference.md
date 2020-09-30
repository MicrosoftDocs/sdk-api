---
UID: NF:cscobj.IOfflineFilesSetting.GetPreference
title: IOfflineFilesSetting::GetPreference (cscobj.h)
description: Retrieves a per-machine or per-user preference associated with a particular Offline Files setting.
helpviewer_keywords: ["GetPreference","GetPreference method [Offline Files]","GetPreference method [Offline Files]","IOfflineFilesSetting interface","IOfflineFilesSetting interface [Offline Files]","GetPreference method","IOfflineFilesSetting.GetPreference","IOfflineFilesSetting::GetPreference","OFFLINEFILES_SETTING_SCOPE_COMPUTER","OFFLINEFILES_SETTING_SCOPE_USER","cscobj/IOfflineFilesSetting::GetPreference","of.iofflinefilessetting_getpreference"]
old-location: of\iofflinefilessetting_getpreference.htm
tech.root: of
ms.assetid: 80bc64f2-2787-42ba-9c36-742964440f74
ms.date: 12/05/2018
ms.keywords: GetPreference, GetPreference method [Offline Files], GetPreference method [Offline Files],IOfflineFilesSetting interface, IOfflineFilesSetting interface [Offline Files],GetPreference method, IOfflineFilesSetting.GetPreference, IOfflineFilesSetting::GetPreference, OFFLINEFILES_SETTING_SCOPE_COMPUTER, OFFLINEFILES_SETTING_SCOPE_USER, cscobj/IOfflineFilesSetting::GetPreference, of.iofflinefilessetting_getpreference
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
 - IOfflineFilesSetting::GetPreference
 - cscobj/IOfflineFilesSetting::GetPreference
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
 - IOfflineFilesSetting.GetPreference
---

# IOfflineFilesSetting::GetPreference


## -description

Retrieves a per-machine or per-user preference associated with a particular Offline Files setting.

## -parameters

### -param pvarValue [out]

If the preference supports one or more values, the returned <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> object contains those values.  If the preference does not support values, the type of the returned <b>VARIANT</b> is <b>VT_EMPTY</b>.

The method initializes the <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> prior to storing the preference value in it.

### -param dwScope [in]

Indicates which preference is to be retrieved.  Must be one of the following.



#### OFFLINEFILES_SETTING_SCOPE_USER (0x00000001)

The per-user preference is to be retrieved.



#### OFFLINEFILES_SETTING_SCOPE_COMPUTER (0x00000002)

The per-machine preference is to be retrieved.

## -returns

<b>S_OK</b> if the preference query is successful or an error value otherwise.

Returns <code>HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)</code> if the preference is currently not applied.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilessetting">IOfflineFilesSetting</a>