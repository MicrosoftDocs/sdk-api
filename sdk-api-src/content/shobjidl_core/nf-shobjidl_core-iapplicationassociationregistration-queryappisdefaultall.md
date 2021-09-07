---
UID: NF:shobjidl_core.IApplicationAssociationRegistration.QueryAppIsDefaultAll
title: IApplicationAssociationRegistration::QueryAppIsDefaultAll (shobjidl_core.h)
description: Determines whether an application owns all of the registered default associations for a given application level. Not intended for use in Windows 8.
helpviewer_keywords: ["IApplicationAssociationRegistration interface [Windows Shell]","QueryAppIsDefaultAll method","IApplicationAssociationRegistration.QueryAppIsDefaultAll","IApplicationAssociationRegistration::QueryAppIsDefaultAll","QueryAppIsDefaultAll","QueryAppIsDefaultAll method [Windows Shell]","QueryAppIsDefaultAll method [Windows Shell]","IApplicationAssociationRegistration interface","_shell_IApplicationAssociationRegistration_QueryAppIsDefaultAll","shell.IApplicationAssociationRegistration_QueryAppIsDefaultAll","shobjidl_core/IApplicationAssociationRegistration::QueryAppIsDefaultAll"]
old-location: shell\IApplicationAssociationRegistration_QueryAppIsDefaultAll.htm
tech.root: shell
ms.assetid: 71073f30-51bc-4522-9bb2-7eb743bca159
ms.date: 12/05/2018
ms.keywords: IApplicationAssociationRegistration interface [Windows Shell],QueryAppIsDefaultAll method, IApplicationAssociationRegistration.QueryAppIsDefaultAll, IApplicationAssociationRegistration::QueryAppIsDefaultAll, QueryAppIsDefaultAll, QueryAppIsDefaultAll method [Windows Shell], QueryAppIsDefaultAll method [Windows Shell],IApplicationAssociationRegistration interface, _shell_IApplicationAssociationRegistration_QueryAppIsDefaultAll, shell.IApplicationAssociationRegistration_QueryAppIsDefaultAll, shobjidl_core/IApplicationAssociationRegistration::QueryAppIsDefaultAll
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
 - IApplicationAssociationRegistration::QueryAppIsDefaultAll
 - shobjidl_core/IApplicationAssociationRegistration::QueryAppIsDefaultAll
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
 - IApplicationAssociationRegistration.QueryAppIsDefaultAll
---

# IApplicationAssociationRegistration::QueryAppIsDefaultAll


## -description

Determines whether an application owns all of the registered default associations for a given application level. Not intended for use in Windows 8.

## -parameters

### -param alQueryLevel [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-associationlevel">ASSOCIATIONLEVEL</a></b>

One of the <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-associationlevel">ASSOCIATIONLEVEL</a> enumeration values that specifies the level of association, such as per-user or machine. This is typically <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-associationlevel">AL_EFFECTIVE</a>.

### -param pszAppRegistryName [in]

Type: <b>LPCWSTR</b>

A pointer to a <b>null</b>-terminated Unicode string that specifies the registered name of the application.

### -param pfDefault [out]

Type: <b>BOOL*</b>

When this method returns, contains <b>TRUE</b> if the application is the default for all <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-associationtype"> association types</a> at the specified <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-associationlevel">ASSOCIATIONLEVEL</a>; 
or <b>FALSE</b> otherwise.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/shell/default-programs">Default Programs</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration">IApplicationAssociationRegistration</a>