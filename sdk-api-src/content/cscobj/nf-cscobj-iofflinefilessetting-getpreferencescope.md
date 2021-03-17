---
UID: NF:cscobj.IOfflineFilesSetting.GetPreferenceScope
title: IOfflineFilesSetting::GetPreferenceScope (cscobj.h)
description: Indicates the scope of the preference associated with this setting.
helpviewer_keywords: ["GetPreferenceScope","GetPreferenceScope method [Offline Files]","GetPreferenceScope method [Offline Files]","IOfflineFilesSetting interface","IOfflineFilesSetting interface [Offline Files]","GetPreferenceScope method","IOfflineFilesSetting.GetPreferenceScope","IOfflineFilesSetting::GetPreferenceScope","OFFLINEFILES_SETTING_SCOPE_COMPUTER","OFFLINEFILES_SETTING_SCOPE_USER","cscobj/IOfflineFilesSetting::GetPreferenceScope","of.iofflinefilessetting_getpreferencescope"]
old-location: of\iofflinefilessetting_getpreferencescope.htm
tech.root: of
ms.assetid: 618a83b7-a86d-4356-8312-7aba8923e8a4
ms.date: 12/05/2018
ms.keywords: GetPreferenceScope, GetPreferenceScope method [Offline Files], GetPreferenceScope method [Offline Files],IOfflineFilesSetting interface, IOfflineFilesSetting interface [Offline Files],GetPreferenceScope method, IOfflineFilesSetting.GetPreferenceScope, IOfflineFilesSetting::GetPreferenceScope, OFFLINEFILES_SETTING_SCOPE_COMPUTER, OFFLINEFILES_SETTING_SCOPE_USER, cscobj/IOfflineFilesSetting::GetPreferenceScope, of.iofflinefilessetting_getpreferencescope
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
 - IOfflineFilesSetting::GetPreferenceScope
 - cscobj/IOfflineFilesSetting::GetPreferenceScope
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
 - IOfflineFilesSetting.GetPreferenceScope
---

# IOfflineFilesSetting::GetPreferenceScope


## -description

Indicates the scope of the preference associated with this setting.

## -parameters

### -param pdwScope [out]

Receives the supported scope of the policy for this setting.  This scope can be one or both of the following values.



#### OFFLINEFILES_SETTING_SCOPE_USER (0x00000001)

The setting supports per-user preference.



#### OFFLINEFILES_SETTING_SCOPE_COMPUTER (0x00000002)

The setting supports per-machine preference.

## -returns

S_OK if the scope is returned successfully or an error value otherwise.

## -remarks

Note that this is an indication of the supported scopes, not of the applied scopes.  For example, a setting may recognize both per-user and per-machine preference yet only the per-user preference has been applied.  In this scenario, this method would return both OFFLINEFILES_SETTING_SCOPE_USER and OFFLINEFILES_SETTING_SCOPE_COMPUTER.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilessetting">IOfflineFilesSetting</a>