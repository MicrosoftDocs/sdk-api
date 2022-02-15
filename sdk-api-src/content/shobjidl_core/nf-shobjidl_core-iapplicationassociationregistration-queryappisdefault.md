---
UID: NF:shobjidl_core.IApplicationAssociationRegistration.QueryAppIsDefault
title: IApplicationAssociationRegistration::QueryAppIsDefault (shobjidl_core.h)
description: Determines whether an application owns the registered default association for a given application level and type. Not intended for use in Windows 8.
helpviewer_keywords: ["IApplicationAssociationRegistration interface [Windows Shell]","QueryAppIsDefault method","IApplicationAssociationRegistration.QueryAppIsDefault","IApplicationAssociationRegistration::QueryAppIsDefault","QueryAppIsDefault","QueryAppIsDefault method [Windows Shell]","QueryAppIsDefault method [Windows Shell]","IApplicationAssociationRegistration interface","_shell_IApplicationAssociationRegistration_QueryAppIsDefault","shell.IApplicationAssociationRegistration_QueryAppIsDefault","shobjidl_core/IApplicationAssociationRegistration::QueryAppIsDefault"]
old-location: shell\IApplicationAssociationRegistration_QueryAppIsDefault.htm
tech.root: shell
ms.assetid: 63127fa4-be09-4dd6-9084-cfde00967279
ms.date: 12/05/2018
ms.keywords: IApplicationAssociationRegistration interface [Windows Shell],QueryAppIsDefault method, IApplicationAssociationRegistration.QueryAppIsDefault, IApplicationAssociationRegistration::QueryAppIsDefault, QueryAppIsDefault, QueryAppIsDefault method [Windows Shell], QueryAppIsDefault method [Windows Shell],IApplicationAssociationRegistration interface, _shell_IApplicationAssociationRegistration_QueryAppIsDefault, shell.IApplicationAssociationRegistration_QueryAppIsDefault, shobjidl_core/IApplicationAssociationRegistration::QueryAppIsDefault
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
 - IApplicationAssociationRegistration::QueryAppIsDefault
 - shobjidl_core/IApplicationAssociationRegistration::QueryAppIsDefault
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
 - IApplicationAssociationRegistration.QueryAppIsDefault
---

# IApplicationAssociationRegistration::QueryAppIsDefault


## -description

Determines whether an application owns the registered default association for a given application level and type. Not intended for use in Windows 8.

## -parameters

### -param pszQuery [in]

Type: <b>LPCWSTR</b>

A pointer to a <b>null</b>-terminated Unicode string that contains the file name extension or protocol of the application, such as .mp3 or http.

### -param atQueryType [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-associationtype">ASSOCIATIONTYPE</a></b>

One of the <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-associationtype">ASSOCIATIONTYPE</a> enumeration values that specifies the type of the application named in <i>pszQuery</i>, such as file name extension or MIME type.

### -param alQueryLevel [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-associationlevel">ASSOCIATIONLEVEL</a></b>

One of the <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-associationlevel">ASSOCIATIONLEVEL</a> enumeration values that specifies the level of association, such as per-user or machine. This is typically <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-associationlevel">AL_EFFECTIVE</a>.

### -param pszAppRegistryName [in]

Type: <b>LPCWSTR</b>

A pointer to a <b>null</b>-terminated Unicode string that specifies the registered name of the application.

### -param pfDefault [out]

Type: <b>BOOL*</b>

 When this method returns, contains <b>TRUE</b> if the application is the default; or <b>FALSE</b> otherwise.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/shell/default-programs">Default Programs</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration">IApplicationAssociationRegistration</a>