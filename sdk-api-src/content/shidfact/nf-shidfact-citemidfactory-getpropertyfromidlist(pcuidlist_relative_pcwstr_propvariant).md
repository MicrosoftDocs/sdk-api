---
UID: NF:shidfact.CItemIDFactory.GetPropertyFromIDList(PCUIDLIST_RELATIVE,PCWSTR,PROPVARIANT)
title: CItemIDFactory::GetPropertyFromIDList(PCUIDLIST_RELATIVE,PCWSTR,PROPVARIANT) (shidfact.h)
description: Gets a property from the IPropertyStore within the IDList as a variant, using the key.helpviewer_keywords: ["CItemIDFactory interface [Windows Shell]","GetPropertyFromIDList method","CItemIDFactory.GetPropertyFromIDList","CItemIDFactory.GetPropertyFromIDList(PCUIDLIST_RELATIVE","PCWSTR","PROPVARIANT)","CItemIDFactory::GetPropertyFromIDList","CItemIDFactory::GetPropertyFromIDList(PCUIDLIST_RELATIVE","PCWSTR","PROPVARIANT)","GetPropertyFromIDList","GetPropertyFromIDList method [Windows Shell]","GetPropertyFromIDList method [Windows Shell]","CItemIDFactory interface","shell.citemidfactory_getpropertyfromidlist_key","shidfact/CItemIDFactory::GetPropertyFromIDList"]
old-location: shell\citemidfactory_getpropertyfromidlist_key.htm
tech.root: shell
ms.assetid: 2BC0557F-57B2-4389-ABC6-9186A4FCF814
ms.date: 12/05/2018
ms.keywords: CItemIDFactory interface [Windows Shell],GetPropertyFromIDList method, CItemIDFactory.GetPropertyFromIDList, CItemIDFactory.GetPropertyFromIDList(PCUIDLIST_RELATIVE,PCWSTR,PROPVARIANT), CItemIDFactory::GetPropertyFromIDList, CItemIDFactory::GetPropertyFromIDList(PCUIDLIST_RELATIVE,PCWSTR,PROPVARIANT), GetPropertyFromIDList, GetPropertyFromIDList method [Windows Shell], GetPropertyFromIDList method [Windows Shell],CItemIDFactory interface, shell.citemidfactory_getpropertyfromidlist_key, shidfact/CItemIDFactory::GetPropertyFromIDList
f1_keywords:
- shidfact/GetPropertyFromIDList.GetPropertyFromIDList
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CItemIDFactory::GetPropertyFromIDList(PCUIDLIST_RELATIVE,PCWSTR,PROPVARIANT)


## -description


Gets a property from the <a href="https://docs.microsoft.com/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> within the IDList as a variant, using the key.


## -parameters




### -param pidl [in]

A PIDL identifying the <a href="https://docs.microsoft.com/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a>.


### -param pszName [in]

The key for the selected property.


### -param pv [out]

When this method returns, contains a pointer to the property. If <i>rkey</i> is not found, <i>pvar</i> will be <b>VT_EMPTY</b>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is useful when using <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsex">IShellFolder2::GetDetailsEx</a>, as is returns a variant rather than a <b>PROPVARIANT</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shidfact/nl-shidfact-citemidfactory">CItemIDFactory</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh289343(v=vs.85)">GetPropertyFromIDList</a>



<a href="https://docs.microsoft.com/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsex">IShellFolder2::GetDetailsEx</a>
 

 

