---
UID: NF:shobjidl_core.IApplicationAssociationRegistration.SetAppAsDefault
title: IApplicationAssociationRegistration::SetAppAsDefault (shobjidl_core.h)
description: Sets an application as the default for a given extension or protocol, provided that the application's publisher matches the current default's. For more information, see Default Programs. Not intended for use in Windows 8.
helpviewer_keywords: ["IApplicationAssociationRegistration interface [Windows Shell]","SetAppAsDefault method","IApplicationAssociationRegistration.SetAppAsDefault","IApplicationAssociationRegistration::SetAppAsDefault","SetAppAsDefault","SetAppAsDefault method [Windows Shell]","SetAppAsDefault method [Windows Shell]","IApplicationAssociationRegistration interface","_shell_IApplicationAssociationRegistration_SetAppAsDefault","shell.IApplicationAssociationRegistration_SetAppAsDefault","shobjidl_core/IApplicationAssociationRegistration::SetAppAsDefault"]
old-location: shell\IApplicationAssociationRegistration_SetAppAsDefault.htm
tech.root: shell
ms.assetid: 30870adb-793f-404f-809c-1ec34a1f6b82
ms.date: 09/17/2019
ms.keywords: IApplicationAssociationRegistration interface [Windows Shell],SetAppAsDefault method, IApplicationAssociationRegistration.SetAppAsDefault, IApplicationAssociationRegistration::SetAppAsDefault, SetAppAsDefault, SetAppAsDefault method [Windows Shell], SetAppAsDefault method [Windows Shell],IApplicationAssociationRegistration interface, _shell_IApplicationAssociationRegistration_SetAppAsDefault, shell.IApplicationAssociationRegistration_SetAppAsDefault, shobjidl_core/IApplicationAssociationRegistration::SetAppAsDefault
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
 - IApplicationAssociationRegistration::SetAppAsDefault
 - shobjidl_core/IApplicationAssociationRegistration::SetAppAsDefault
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
 - IApplicationAssociationRegistration.SetAppAsDefault
---

# IApplicationAssociationRegistration::SetAppAsDefault


## -description

Sets an application as the default for a given extension or protocol, provided that the application's publisher matches the current default's. For more information, see <a href="/windows/desktop/shell/default-programs">Default Programs</a>. Not intended for use in Windows 8.

## -parameters

### -param progId [in]

Type: <b>LPCWSTR</b>

A pointer to a <b>null</b>-terminated Unicode string that specifies the application's ProgID.

### -param extOrUriScheme [in]

Type: <b>LPCWSTR</b>

A pointer to a <b>null</b>-terminated Unicode string that contains the file name extension or protocol of the application, such as .mp3 or http.

### -param atSetType [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-associationtype">ASSOCIATIONTYPE</a></b>

One of the <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-associationtype">ASSOCIATIONTYPE</a> enumeration values that specifies the type of the application named in <i>extOrUriScheme</i>, such as file name extension or MIME type.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code. In particular, if the application's publisher doesn't match the default's, this method returns <b>E_ACCESSDENIED</b>.

## -see-also

<a href="/windows/desktop/shell/default-programs">Default Programs</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration">IApplicationAssociationRegistration</a>