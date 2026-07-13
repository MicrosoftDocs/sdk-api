---
UID: NF:uiribbon.IUICollection.Insert
title: IUICollection::Insert (uiribbon.h)
description: Inserts an item into the IUICollection at the specified index.
helpviewer_keywords: ["IUICollection interface [Windows Ribbon]","Insert method","IUICollection.Insert","IUICollection::Insert","Insert","Insert method [Windows Ribbon]","Insert method [Windows Ribbon]","IUICollection interface","scenicintent_IUICollection_Insert","uiribbon/IUICollection::Insert","windowsribbon.windowsribbon_iuicollection_insert"]
old-location: windowsribbon\windowsribbon_iuicollection_insert.htm
tech.root: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuicollection\insert.htm
ms.date: 12/05/2018
ms.keywords: IUICollection interface [Windows Ribbon],Insert method, IUICollection.Insert, IUICollection::Insert, Insert, Insert method [Windows Ribbon], Insert method [Windows Ribbon],IUICollection interface, scenicintent_IUICollection_Insert, uiribbon/IUICollection::Insert, windowsribbon.windowsribbon_iuicollection_insert
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
 - IUICollection::Insert
 - uiribbon/IUICollection::Insert
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
 - IUICollection.Insert
---

# IUICollection::Insert


## -description

Inserts an item into the <a href="/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection">IUICollection</a> at the specified index.

## -parameters

### -param index [in]

Type: <b>UINT32</b>

The zero-based index at which <i>item</i> is inserted into the <a href="/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection">IUICollection</a>.

### -param item [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

Pointer to the item that is added to the <a href="/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection">IUICollection</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/windowsribbon/windowsribbon-gallerysample">Gallery Sample</a>



<a href="/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection">IUICollection</a>