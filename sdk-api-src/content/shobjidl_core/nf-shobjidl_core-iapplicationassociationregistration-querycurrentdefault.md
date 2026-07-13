---
UID: NF:shobjidl_core.IApplicationAssociationRegistration.QueryCurrentDefault
title: IApplicationAssociationRegistration::QueryCurrentDefault (shobjidl_core.h)
description: Determines the default application for a given association type. This is the default application launched by ShellExecute for that type.
helpviewer_keywords: ["IApplicationAssociationRegistration interface [Windows Shell]","QueryCurrentDefault method","IApplicationAssociationRegistration.QueryCurrentDefault","IApplicationAssociationRegistration::QueryCurrentDefault","QueryCurrentDefault","QueryCurrentDefault method [Windows Shell]","QueryCurrentDefault method [Windows Shell]","IApplicationAssociationRegistration interface","_shell_IApplicationAssociationRegistration_QueryCurrentDefault","shell.IApplicationAssociationRegistration_QueryCurrentDefault","shobjidl_core/IApplicationAssociationRegistration::QueryCurrentDefault"]
old-location: shell\IApplicationAssociationRegistration_QueryCurrentDefault.htm
tech.root: shell
ms.assetid: af6bd032-1457-4805-9844-87b5efb5ba21
ms.date: 12/05/2018
ms.keywords: IApplicationAssociationRegistration interface [Windows Shell],QueryCurrentDefault method, IApplicationAssociationRegistration.QueryCurrentDefault, IApplicationAssociationRegistration::QueryCurrentDefault, QueryCurrentDefault, QueryCurrentDefault method [Windows Shell], QueryCurrentDefault method [Windows Shell],IApplicationAssociationRegistration interface, _shell_IApplicationAssociationRegistration_QueryCurrentDefault, shell.IApplicationAssociationRegistration_QueryCurrentDefault, shobjidl_core/IApplicationAssociationRegistration::QueryCurrentDefault
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
 - IApplicationAssociationRegistration::QueryCurrentDefault
 - shobjidl_core/IApplicationAssociationRegistration::QueryCurrentDefault
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IApplicationAssociationRegistration.QueryCurrentDefault
---

# IApplicationAssociationRegistration::QueryCurrentDefault


## -description

Determines the default application for a given association type. This is the default application launched by <a href="/windows/desktop/api/shellapi/nf-shellapi-shellexecutea">ShellExecute</a> for that type.

## -parameters

### -param pszQuery [in]

Type: <b>LPCWSTR</b>

A pointer to a null-terminated, Unicode string that contains the file name extension or protocol, such as .mp3 or http.

### -param atQueryType [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-associationtype">ASSOCIATIONTYPE</a></b>

One of the <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-associationtype">ASSOCIATIONTYPE</a> enumeration values that specifies the type of association, such as extension or MIME type.

### -param alQueryLevel [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-associationlevel">ASSOCIATIONLEVEL</a></b>

One of the <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-associationlevel">ASSOCIATIONLEVEL</a> enumeration values that specifies the level of association, such as per-user or machine. This is typically <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-associationlevel">AL_EFFECTIVE</a>.

### -param ppszAssociation [out]

Type: <b>LPWSTR*</b>

When this method returns, contains the address of a pointer to the ProgID that identifies the current default association.

<div class="alert"><b>Note</b>  It is the responsibility of the calling application to release the string through <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.</div>
<div> </div>

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The string produced is typically a ProgID matching one of the ProgIDs associated with a registered application, but there are a few exceptions: If the string returned is a machine default protocol, it is a legacy string indicating a command line to a .exe handler instead of a ProgID. Similarly, if returning a machine default MIME type, it returns a legacy class identifier (CLSID) string instead of a ProgID.

## -see-also

<a href="/windows/desktop/shell/default-programs">Default Programs</a>

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration">IApplicationAssociationRegistration</a>
