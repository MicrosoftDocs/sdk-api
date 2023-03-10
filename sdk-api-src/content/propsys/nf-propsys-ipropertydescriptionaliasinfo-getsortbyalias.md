---
UID: NF:propsys.IPropertyDescriptionAliasInfo.GetSortByAlias
title: IPropertyDescriptionAliasInfo::GetSortByAlias (propsys.h)
description: Gets the address of a pointer to the IPropertyDescription interface containing the primary sort column.
helpviewer_keywords: ["GetSortByAlias","GetSortByAlias method [Windows Properties]","GetSortByAlias method [Windows Properties]","IPropertyDescriptionAliasInfo interface","IPropertyDescriptionAliasInfo interface [Windows Properties]","GetSortByAlias method","IPropertyDescriptionAliasInfo.GetSortByAlias","IPropertyDescriptionAliasInfo::GetSortByAlias","_shell_IPropertyDescriptionAliasInfo_GetSortByAlias","properties.IPropertyDescriptionAliasInfo_GetSortByAlias","propsys/IPropertyDescriptionAliasInfo::GetSortByAlias","shell.IPropertyDescriptionAliasInfo_GetSortByAlias"]
old-location: properties\IPropertyDescriptionAliasInfo_GetSortByAlias.htm
tech.root: properties
ms.assetid: 22a60d4e-d7e7-4a14-a56a-5325a5dae2eb
ms.date: 12/05/2018
ms.keywords: GetSortByAlias, GetSortByAlias method [Windows Properties], GetSortByAlias method [Windows Properties],IPropertyDescriptionAliasInfo interface, IPropertyDescriptionAliasInfo interface [Windows Properties],GetSortByAlias method, IPropertyDescriptionAliasInfo.GetSortByAlias, IPropertyDescriptionAliasInfo::GetSortByAlias, _shell_IPropertyDescriptionAliasInfo_GetSortByAlias, properties.IPropertyDescriptionAliasInfo_GetSortByAlias, propsys/IPropertyDescriptionAliasInfo::GetSortByAlias, shell.IPropertyDescriptionAliasInfo_GetSortByAlias
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
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
 - IPropertyDescriptionAliasInfo::GetSortByAlias
 - propsys/IPropertyDescriptionAliasInfo::GetSortByAlias
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.h
api_name:
 - IPropertyDescriptionAliasInfo.GetSortByAlias
---

# IPropertyDescriptionAliasInfo::GetSortByAlias


## -description

Gets the address of a pointer to the <a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescription">IPropertyDescription</a> interface containing the primary sort column.

## -parameters

### -param riid [in]

Type: <b>REFIID</b>

A reference to the identifier of the requested <a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescription">IPropertyDescription</a> interface.

### -param ppv [out]

Type: <b>void**</b>

When this method returns successfully, contains the address of a pointer to the <a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescription">IPropertyDescription</a> interface for the calling object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescriptionaliasinfo">IPropertyDescriptionAliasInfo</a>



<a href="/windows/desktop/api/propsys/nf-propsys-ipropertydescriptionaliasinfo-getadditionalsortbyaliases">IPropertyDescriptionAliasInfo::GetAdditionalSortByAliases</a>