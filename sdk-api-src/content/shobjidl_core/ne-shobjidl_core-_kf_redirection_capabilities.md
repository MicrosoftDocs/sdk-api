---
UID: NE:shobjidl_core._KF_REDIRECTION_CAPABILITIES
title: _KF_REDIRECTION_CAPABILITIES (shobjidl_core.h)
description: Flags that specify the current redirection capabilities of a known folder. Used by IKnownFolder::GetRedirectionCapabilities.
helpviewer_keywords: ["KF_REDIRECTION_CAPABILITIES","KF_REDIRECTION_CAPABILITIES enumeration [Windows Shell]","KF_REDIRECTION_CAPABILITIES_ALLOW_ALL","KF_REDIRECTION_CAPABILITIES_DENY_ALL","KF_REDIRECTION_CAPABILITIES_DENY_PERMISSIONS","KF_REDIRECTION_CAPABILITIES_DENY_POLICY","KF_REDIRECTION_CAPABILITIES_DENY_POLICY_REDIRECTED","KF_REDIRECTION_CAPABILITIES_REDIRECTABLE","_KF_REDIRECTION_CAPABILITIES","_shell_KF_REDIRECTION_CAPABILITIES","shell.KF_REDIRECTION_CAPABILITIES","shobjidl_core/KF_REDIRECTION_CAPABILITIES","shobjidl_core/KF_REDIRECTION_CAPABILITIES_ALLOW_ALL","shobjidl_core/KF_REDIRECTION_CAPABILITIES_DENY_ALL","shobjidl_core/KF_REDIRECTION_CAPABILITIES_DENY_PERMISSIONS","shobjidl_core/KF_REDIRECTION_CAPABILITIES_DENY_POLICY","shobjidl_core/KF_REDIRECTION_CAPABILITIES_DENY_POLICY_REDIRECTED","shobjidl_core/KF_REDIRECTION_CAPABILITIES_REDIRECTABLE"]
old-location: shell\KF_REDIRECTION_CAPABILITIES.htm
tech.root: shell
ms.assetid: 3c9830fc-75cd-4b11-bfb4-55b66063614b
ms.date: 12/05/2018
ms.keywords: KF_REDIRECTION_CAPABILITIES, KF_REDIRECTION_CAPABILITIES enumeration [Windows Shell], KF_REDIRECTION_CAPABILITIES_ALLOW_ALL, KF_REDIRECTION_CAPABILITIES_DENY_ALL, KF_REDIRECTION_CAPABILITIES_DENY_PERMISSIONS, KF_REDIRECTION_CAPABILITIES_DENY_POLICY, KF_REDIRECTION_CAPABILITIES_DENY_POLICY_REDIRECTED, KF_REDIRECTION_CAPABILITIES_REDIRECTABLE, _KF_REDIRECTION_CAPABILITIES, _shell_KF_REDIRECTION_CAPABILITIES, shell.KF_REDIRECTION_CAPABILITIES, shobjidl_core/KF_REDIRECTION_CAPABILITIES, shobjidl_core/KF_REDIRECTION_CAPABILITIES_ALLOW_ALL, shobjidl_core/KF_REDIRECTION_CAPABILITIES_DENY_ALL, shobjidl_core/KF_REDIRECTION_CAPABILITIES_DENY_PERMISSIONS, shobjidl_core/KF_REDIRECTION_CAPABILITIES_DENY_POLICY, shobjidl_core/KF_REDIRECTION_CAPABILITIES_DENY_POLICY_REDIRECTED, shobjidl_core/KF_REDIRECTION_CAPABILITIES_REDIRECTABLE
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _KF_REDIRECTION_CAPABILITIES
 - shobjidl_core/_KF_REDIRECTION_CAPABILITIES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - KF_REDIRECTION_CAPABILITIES
---

# _KF_REDIRECTION_CAPABILITIES enumeration


## -description

Flags that specify the current redirection capabilities of a known folder. Used by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getredirectioncapabilities">IKnownFolder::GetRedirectionCapabilities</a>.

## -enum-fields

### -field KF_REDIRECTION_CAPABILITIES_ALLOW_ALL:0xff

The folder can be redirected if any of the bits in the lower byte of the value are set but no DENY flag is set. DENY flags are found in the upper byte of the value.

### -field KF_REDIRECTION_CAPABILITIES_REDIRECTABLE:0x1

The folder can be redirected. Currently, redirection exists for only common and user folders; fixed and virtual folders cannot be redirected.

### -field KF_REDIRECTION_CAPABILITIES_DENY_ALL:0xfff00

Redirection is not allowed.

### -field KF_REDIRECTION_CAPABILITIES_DENY_POLICY_REDIRECTED:0x100

The folder cannot be redirected because it is already redirected by group policy.

### -field KF_REDIRECTION_CAPABILITIES_DENY_POLICY:0x200

The folder cannot be redirected because the policy prohibits redirecting this folder.

### -field KF_REDIRECTION_CAPABILITIES_DENY_PERMISSIONS:0x400

The folder cannot be redirected because the calling application does not have sufficient permissions.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dd940364(v=vs.85)">Known Folders Sample</a>
