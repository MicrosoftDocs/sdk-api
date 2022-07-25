---
UID: NF:shidfact.CItemIDFactory.GetPropertyStorageFromIDList
title: CItemIDFactory::GetPropertyStorageFromIDList (shidfact.h)
description: Create an instance of the IPropertyStore based on the serialized property storage associated with the first ItemID.
helpviewer_keywords: ["CItemIDFactory interface [Windows Shell]","GetPropertyStorageFromIDList method","CItemIDFactory.GetPropertyStorageFromIDList","CItemIDFactory::GetPropertyStorageFromIDList","GetPropertyStorageFromIDList","GetPropertyStorageFromIDList method [Windows Shell]","GetPropertyStorageFromIDList method [Windows Shell]","CItemIDFactory interface","shell.citemidfactory_getpropertystoragefromidlist","shidfact/CItemIDFactory::GetPropertyStorageFromIDList"]
old-location: shell\citemidfactory_getpropertystoragefromidlist.htm
tech.root: shell
ms.assetid: 50E8F4F9-1E7B-4314-9AFB-1CA0795776FE
ms.date: 12/05/2018
ms.keywords: CItemIDFactory interface [Windows Shell],GetPropertyStorageFromIDList method, CItemIDFactory.GetPropertyStorageFromIDList, CItemIDFactory::GetPropertyStorageFromIDList, GetPropertyStorageFromIDList, GetPropertyStorageFromIDList method [Windows Shell], GetPropertyStorageFromIDList method [Windows Shell],CItemIDFactory interface, shell.citemidfactory_getpropertystoragefromidlist, shidfact/CItemIDFactory::GetPropertyStorageFromIDList
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
 - CItemIDFactory::GetPropertyStorageFromIDList
 - shidfact/CItemIDFactory::GetPropertyStorageFromIDList
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
 - CItemIDFactory.GetPropertyStorageFromIDList
---

# CItemIDFactory::GetPropertyStorageFromIDList


## -description

create an instance of the <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> based on the serialized property storage associated with the first ItemID.

## -parameters

### -param pidl [in]

A PIDL containing the serialized property storage.

### -param riid [in]

A reference to the IID of the <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> that is obtained by using __uuidof(IPropertyStore).

### -param ppv [out]

When this method returns, contains the address of a pointer to a new <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shidfact/nl-shidfact-citemidfactory">CItemIDFactory</a>



<a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a>