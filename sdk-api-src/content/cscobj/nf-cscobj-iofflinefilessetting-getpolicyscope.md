---
UID: NF:cscobj.IOfflineFilesSetting.GetPolicyScope
title: IOfflineFilesSetting::GetPolicyScope (cscobj.h)
description: Retrieves the scope of the policy associated with this setting.
helpviewer_keywords: ["GetPolicyScope","GetPolicyScope method [Offline Files]","GetPolicyScope method [Offline Files]","IOfflineFilesSetting interface","IOfflineFilesSetting interface [Offline Files]","GetPolicyScope method","IOfflineFilesSetting.GetPolicyScope","IOfflineFilesSetting::GetPolicyScope","OFFLINEFILES_SETTING_SCOPE_COMPUTER","OFFLINEFILES_SETTING_SCOPE_USER","cscobj/IOfflineFilesSetting::GetPolicyScope","of.iofflinefilessetting_getpolicyscope"]
old-location: of\iofflinefilessetting_getpolicyscope.htm
tech.root: of
ms.assetid: 29f6d96f-c873-4cc3-88f2-cd075b3ec004
ms.date: 12/05/2018
ms.keywords: GetPolicyScope, GetPolicyScope method [Offline Files], GetPolicyScope method [Offline Files],IOfflineFilesSetting interface, IOfflineFilesSetting interface [Offline Files],GetPolicyScope method, IOfflineFilesSetting.GetPolicyScope, IOfflineFilesSetting::GetPolicyScope, OFFLINEFILES_SETTING_SCOPE_COMPUTER, OFFLINEFILES_SETTING_SCOPE_USER, cscobj/IOfflineFilesSetting::GetPolicyScope, of.iofflinefilessetting_getpolicyscope
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
 - IOfflineFilesSetting::GetPolicyScope
 - cscobj/IOfflineFilesSetting::GetPolicyScope
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
 - IOfflineFilesSetting.GetPolicyScope
---

# IOfflineFilesSetting::GetPolicyScope


## -description

Retrieves the scope of the policy associated with this setting.

## -parameters

### -param pdwScope [out]

Receives the supported scope of the policy for this setting.  This scope can be one or both of the following values.



#### OFFLINEFILES_SETTING_SCOPE_USER (0x00000001)

The setting supports per-user policy.



#### OFFLINEFILES_SETTING_SCOPE_COMPUTER (0x00000002)

The setting supports per-machine policy.

## -returns

S_OK if the scope is returned successfully or an error value otherwise.

## -remarks

Note that this is an indication of the supported scopes, not of the applied scopes.  For example, a setting may recognize both per-user and per-machine policy yet only the per-user policy has been applied.  In this scenario, this API would return both OFFLINEFILES_SETTING_SCOPE_USER and OFFLINEFILES_SETTING_SCOPE_COMPUTER.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilessetting">IOfflineFilesSetting</a>