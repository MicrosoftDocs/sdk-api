---
UID: NF:shidfact.CItemIDFactory.GetPropertyFromIDList(PCUIDLIST_RELATIVE,PCWSTR,VARIANT)
title: CItemIDFactory::GetPropertyFromIDList(PCUIDLIST_RELATIVE,PCWSTR,VARIANT) (shidfact.h)
description: Gets a property from the IPropertyStore within the IDList as a variant, using the key. (overload 2/4)
helpviewer_keywords: ["CItemIDFactory interface [Windows Shell]","GetPropertyFromIDList method","CItemIDFactory.GetPropertyFromIDList","CItemIDFactory.GetPropertyFromIDList(PCUIDLIST_RELATIVE","PCWSTR","VARIANT)","CItemIDFactory::GetPropertyFromIDList","CItemIDFactory::GetPropertyFromIDList(PCUIDLIST_RELATIVE","PCWSTR","VARIANT)","GetPropertyFromIDList","GetPropertyFromIDList method [Windows Shell]","GetPropertyFromIDList method [Windows Shell]","CItemIDFactory interface","shell.citemidfactory_getpropertyfromidlist_key","shidfact/CItemIDFactory::GetPropertyFromIDList"]
old-location: shell\citemidfactory_getpropertyfromidlist_key.htm
tech.root: shell
ms.assetid: 2BC0557F-57B2-4389-ABC6-9186A4FCF814
ms.date: 12/05/2018
ms.keywords: CItemIDFactory interface [Windows Shell],GetPropertyFromIDList method, CItemIDFactory.GetPropertyFromIDList, CItemIDFactory.GetPropertyFromIDList(PCUIDLIST_RELATIVE,PCWSTR,VARIANT), CItemIDFactory::GetPropertyFromIDList, CItemIDFactory::GetPropertyFromIDList(PCUIDLIST_RELATIVE,PCWSTR,VARIANT), GetPropertyFromIDList, GetPropertyFromIDList method [Windows Shell], GetPropertyFromIDList method [Windows Shell],CItemIDFactory interface, shell.citemidfactory_getpropertyfromidlist_key, shidfact/CItemIDFactory::GetPropertyFromIDList
req.header: shidfact.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CItemIDFactory::GetPropertyFromIDList
 - shidfact/CItemIDFactory::GetPropertyFromIDList
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shidfact.h
api_name:
 - GetPropertyFromIDList.GetPropertyFromIDList
 - CItemIDFactory.GetPropertyFromIDList
---

# CItemIDFactory::GetPropertyFromIDList(PCUIDLIST_RELATIVE,PCWSTR,VARIANT)


## -description

Gets a property from the <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> within the IDList as a variant, using the key.

## -parameters

### -param pidl [in]

A PIDL identifying the <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a>.

### -param pszName [in]

The key for the selected property.

### -param pvar

When this method returns, contains a pointer to the property. If <i>rkey</i> is not found, <i>pvar</i> will be <b>VT_EMPTY</b>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is useful when using <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsex">IShellFolder2::GetDetailsEx</a>, as is returns a variant rather than a <b>PROPVARIANT</b>.

## -see-also

<a href="/windows/desktop/api/shidfact/nl-shidfact-citemidfactory">CItemIDFactory</a>



<a href="/previous-versions/windows/desktop/legacy/hh289343(v=vs.85)">GetPropertyFromIDList</a>



<a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsex">IShellFolder2::GetDetailsEx</a>
