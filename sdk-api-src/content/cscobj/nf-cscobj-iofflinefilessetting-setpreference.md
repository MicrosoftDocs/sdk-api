---
UID: NF:cscobj.IOfflineFilesSetting.SetPreference
title: IOfflineFilesSetting::SetPreference (cscobj.h)
description: Sets a per-computer or per-user preference associated with an Offline Files setting.
helpviewer_keywords: ["IOfflineFilesSetting interface [Offline Files]","SetPreference method","IOfflineFilesSetting.SetPreference","IOfflineFilesSetting::SetPreference","OFFLINEFILES_SETTING_SCOPE_COMPUTER","OFFLINEFILES_SETTING_SCOPE_USER","SetPreference","SetPreference method [Offline Files]","SetPreference method [Offline Files]","IOfflineFilesSetting interface","cscobj/IOfflineFilesSetting::SetPreference","of.iofflinefilessetting_setpreference"]
old-location: of\iofflinefilessetting_setpreference.htm
tech.root: of
ms.assetid: a5dc0522-4a1b-450f-bddb-17e67007f809
ms.date: 12/05/2018
ms.keywords: IOfflineFilesSetting interface [Offline Files],SetPreference method, IOfflineFilesSetting.SetPreference, IOfflineFilesSetting::SetPreference, OFFLINEFILES_SETTING_SCOPE_COMPUTER, OFFLINEFILES_SETTING_SCOPE_USER, SetPreference, SetPreference method [Offline Files], SetPreference method [Offline Files],IOfflineFilesSetting interface, cscobj/IOfflineFilesSetting::SetPreference, of.iofflinefilessetting_setpreference
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
 - IOfflineFilesSetting::SetPreference
 - cscobj/IOfflineFilesSetting::SetPreference
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
 - IOfflineFilesSetting.SetPreference
---

# IOfflineFilesSetting::SetPreference


## -description

Sets a per-computer or per-user preference associated with an Offline Files setting.

## -parameters

### -param pvarValue [in]

Specifies the value associated with the preference.

If multiple values are associated with the preference, the <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> type includes <b>VT_ARRAY</b> and the values are stored in a <b>SAFEARRAY</b>.

### -param dwScope [in]

Indicates if the preference to be set is per-user or per-machine.  Must be one of the following.



#### OFFLINEFILES_SETTING_SCOPE_USER (0x00000001)

The per-user preference is to be set.



#### OFFLINEFILES_SETTING_SCOPE_COMPUTER (0x00000002)

The per-machine preference is to be set.

## -returns

<b>S_OK</b> if the preference is set successfully or an error value otherwise.

Returns <code>HRESULT_FROM_WIN32(ERROR_INVALID_PARAMETER)</code> if one or more data values specified via <i>pvtValue</i> are not valid.

Returns <code>HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)</code> if the caller is trying to set a per-machine preference and is not a local administrator.

Returns <code>HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)</code> if a scope is specified that is not supported by the preference.

## -remarks

This method requires system administrator privileges if the preference is a per-machine preference.

It is important to note that policy cannot be set through the Offline Files API.  Policy can be set only through the Group Policy mechanism.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilessetting">IOfflineFilesSetting</a>