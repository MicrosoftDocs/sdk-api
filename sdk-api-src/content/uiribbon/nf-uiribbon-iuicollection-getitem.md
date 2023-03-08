---
UID: NF:uiribbon.IUICollection.GetItem
title: IUICollection::GetItem (uiribbon.h)
description: Retrieves an item from the IUICollection at the specified index.
helpviewer_keywords: ["GetItem","GetItem method [Windows Ribbon]","GetItem method [Windows Ribbon]","IUICollection interface","IUICollection interface [Windows Ribbon]","GetItem method","IUICollection.GetItem","IUICollection::GetItem","scenicintent_IUICollection_GetItem","uiribbon/IUICollection::GetItem","windowsribbon.windowsribbon_iuicollection_getitem"]
old-location: windowsribbon\windowsribbon_iuicollection_getitem.htm
tech.root: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuicollection\getitem.htm
ms.date: 12/05/2018
ms.keywords: GetItem, GetItem method [Windows Ribbon], GetItem method [Windows Ribbon],IUICollection interface, IUICollection interface [Windows Ribbon],GetItem method, IUICollection.GetItem, IUICollection::GetItem, scenicintent_IUICollection_GetItem, uiribbon/IUICollection::GetItem, windowsribbon.windowsribbon_iuicollection_getitem
req.header: uiribbon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Uiribbon.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Mshtml.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: Windows UI
ms.custom: 19H1
f1_keywords:
 - IUICollection::GetItem
 - uiribbon/IUICollection::GetItem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mshtml.dll
api_name:
 - IUICollection.GetItem
---

# IUICollection::GetItem


## -description

Retrieves an item from the <a href="/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection">IUICollection</a> at the specified index.

## -parameters

### -param index [in]

Type: <b>UINT32</b>

The zero-based index of <i>item</i> to retrieve from the <a href="/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection">IUICollection</a>.

### -param item [out]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>**</b>

When this method returns, contains the address of a pointer variable that receives the item.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/windowsribbon/windowsribbon-gallerysample">Gallery Sample</a>



<a href="/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection">IUICollection</a>