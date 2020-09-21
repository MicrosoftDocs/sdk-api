---
UID: NF:cscobj.IOfflineFilesSetting.GetPolicy
title: IOfflineFilesSetting::GetPolicy (cscobj.h)
description: Retrieves a policy associated with a particular Offline Files setting.
helpviewer_keywords: ["GetPolicy","GetPolicy method [Offline Files]","GetPolicy method [Offline Files]","IOfflineFilesSetting interface","IOfflineFilesSetting interface [Offline Files]","GetPolicy method","IOfflineFilesSetting.GetPolicy","IOfflineFilesSetting::GetPolicy","OFFLINEFILES_SETTING_SCOPE_COMPUTER","OFFLINEFILES_SETTING_SCOPE_USER","cscobj/IOfflineFilesSetting::GetPolicy","of.iofflinefilessetting_getpolicy"]
old-location: of\iofflinefilessetting_getpolicy.htm
tech.root: of
ms.assetid: b7f7f8f5-2640-4770-a7ba-230cca8a9575
ms.date: 12/05/2018
ms.keywords: GetPolicy, GetPolicy method [Offline Files], GetPolicy method [Offline Files],IOfflineFilesSetting interface, IOfflineFilesSetting interface [Offline Files],GetPolicy method, IOfflineFilesSetting.GetPolicy, IOfflineFilesSetting::GetPolicy, OFFLINEFILES_SETTING_SCOPE_COMPUTER, OFFLINEFILES_SETTING_SCOPE_USER, cscobj/IOfflineFilesSetting::GetPolicy, of.iofflinefilessetting_getpolicy
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
 - IOfflineFilesSetting::GetPolicy
 - cscobj/IOfflineFilesSetting::GetPolicy
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
 - IOfflineFilesSetting.GetPolicy
---

# IOfflineFilesSetting::GetPolicy


## -description

Retrieves a policy associated with a particular Offline Files setting.

## -parameters

### -param pvarValue [out]

If the policy supports one or more values, the returned <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> object contains those values.  If the policy does not support values, the type of the returned <b>VARIANT</b> is <b>VT_EMPTY</b>.

The method initializes the <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> prior to storing the policy value in it.

### -param dwScope [in]

Indicates which policy is to be retrieved.  Must be one of the following.

<div class="alert"><b>Note</b>  Note that not all settings have an associated policy and those that do might not support both per-machine and per-user policy.</div>
<div> </div>


#### OFFLINEFILES_SETTING_SCOPE_USER (0x00000001)

The per-user policy is to be retrieved.



#### OFFLINEFILES_SETTING_SCOPE_COMPUTER (0x00000002)

The per-machine policy is to be retrieved.

## -returns

<b>S_OK</b> if the policy is read successfully or an error value otherwise.

Returns <code>HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)</code> if the setting does not support the requested policy.

Returns <code>HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)</code> if the requested policy is not currently applied.

## -remarks

It is important to note that policy cannot be set through the Offline Files API.  Policy can be set only through the Group Policy mechanism.  The Offline Files API only supports querying policy values.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilessetting">IOfflineFilesSetting</a>