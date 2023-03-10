---
UID: NF:uiribbon.IUICollection.RemoveAt
title: IUICollection::RemoveAt (uiribbon.h)
description: Removes an item from the IUICollection at the specified index.
helpviewer_keywords: ["IUICollection interface [Windows Ribbon]","RemoveAt method","IUICollection.RemoveAt","IUICollection::RemoveAt","RemoveAt","RemoveAt method [Windows Ribbon]","RemoveAt method [Windows Ribbon]","IUICollection interface","scenicintent_IUICollection_RemoveAt","uiribbon/IUICollection::RemoveAt","windowsribbon.windowsribbon_iuicollection_removeat"]
old-location: windowsribbon\windowsribbon_iuicollection_removeat.htm
tech.root: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuicollection\removeat.htm
ms.date: 12/05/2018
ms.keywords: IUICollection interface [Windows Ribbon],RemoveAt method, IUICollection.RemoveAt, IUICollection::RemoveAt, RemoveAt, RemoveAt method [Windows Ribbon], RemoveAt method [Windows Ribbon],IUICollection interface, scenicintent_IUICollection_RemoveAt, uiribbon/IUICollection::RemoveAt, windowsribbon.windowsribbon_iuicollection_removeat
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
 - IUICollection::RemoveAt
 - uiribbon/IUICollection::RemoveAt
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
 - IUICollection.RemoveAt
---

# IUICollection::RemoveAt


## -description

Removes an item from the <a href="/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection">IUICollection</a> at the specified index.

## -parameters

### -param index [in]

Type: <b>UINT32</b>

The zero-based index of the item to remove from the <a href="/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection">IUICollection</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/windowsribbon/windowsribbon-gallerysample">Gallery Sample</a>



<a href="/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection">IUICollection</a>