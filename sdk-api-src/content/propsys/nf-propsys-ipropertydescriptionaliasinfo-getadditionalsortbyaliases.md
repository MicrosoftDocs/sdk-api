---
UID: NF:propsys.IPropertyDescriptionAliasInfo.GetAdditionalSortByAliases
title: IPropertyDescriptionAliasInfo::GetAdditionalSortByAliases (propsys.h)
description: Gets the address of a pointer to the IPropertyDescriptionList interface, which contains additional sort column values.
helpviewer_keywords: ["GetAdditionalSortByAliases","GetAdditionalSortByAliases method [Windows Properties]","GetAdditionalSortByAliases method [Windows Properties]","IPropertyDescriptionAliasInfo interface","IPropertyDescriptionAliasInfo interface [Windows Properties]","GetAdditionalSortByAliases method","IPropertyDescriptionAliasInfo.GetAdditionalSortByAliases","IPropertyDescriptionAliasInfo::GetAdditionalSortByAliases","_shell_IPropertyDescriptionAliasInfo_GetAdditionalSortByAliases","properties.IPropertyDescriptionAliasInfo_GetAdditionalSortByAliases","propsys/IPropertyDescriptionAliasInfo::GetAdditionalSortByAliases","shell.IPropertyDescriptionAliasInfo_GetAdditionalSortByAliases"]
old-location: properties\IPropertyDescriptionAliasInfo_GetAdditionalSortByAliases.htm
tech.root: properties
ms.assetid: fb7c105b-6e81-4837-ad00-8886abbe108f
ms.date: 12/05/2018
ms.keywords: GetAdditionalSortByAliases, GetAdditionalSortByAliases method [Windows Properties], GetAdditionalSortByAliases method [Windows Properties],IPropertyDescriptionAliasInfo interface, IPropertyDescriptionAliasInfo interface [Windows Properties],GetAdditionalSortByAliases method, IPropertyDescriptionAliasInfo.GetAdditionalSortByAliases, IPropertyDescriptionAliasInfo::GetAdditionalSortByAliases, _shell_IPropertyDescriptionAliasInfo_GetAdditionalSortByAliases, properties.IPropertyDescriptionAliasInfo_GetAdditionalSortByAliases, propsys/IPropertyDescriptionAliasInfo::GetAdditionalSortByAliases, shell.IPropertyDescriptionAliasInfo_GetAdditionalSortByAliases
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
 - IPropertyDescriptionAliasInfo::GetAdditionalSortByAliases
 - propsys/IPropertyDescriptionAliasInfo::GetAdditionalSortByAliases
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
 - IPropertyDescriptionAliasInfo.GetAdditionalSortByAliases
---

# IPropertyDescriptionAliasInfo::GetAdditionalSortByAliases


## -description

Gets the address of a pointer to the <a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescriptionlist">IPropertyDescriptionList</a> interface, which contains additional sort column values.

## -parameters

### -param riid [in]

Type: <b>REFIID</b>

A reference to the identifier of the requested <a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescriptionlist">IPropertyDescriptionList</a> interface.

### -param ppv [out]

Type: <b>void**</b>

When this method returns successfully, contains the address of a pointer to an <a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescriptionlist">IPropertyDescriptionList</a> interface.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The following is an example usage for this method. When sorting by System.Author: System.DateModified, System.DateCreated, and System.ItemNameDisplay may be used as secondary sort columns.  This ensures a unique sort order (for System.Author) and is used to provide a more consistent user experience.


 Calling applications include any UI that wants the secondary sort columns for a given property.

## -see-also

<a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescriptionaliasinfo">IPropertyDescriptionAliasInfo</a>



<a href="/windows/desktop/api/propsys/nf-propsys-ipropertydescriptionaliasinfo-getsortbyalias">IPropertyDescriptionAliasInfo::GetSortByAlias</a>