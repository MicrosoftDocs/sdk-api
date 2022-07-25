---
UID: NF:uiribbon.IUICollection.Add
title: IUICollection::Add (uiribbon.h)
description: Adds an item to the end of the IUICollection.
helpviewer_keywords: ["Add","Add method [Windows Ribbon]","Add method [Windows Ribbon]","IUICollection interface","IUICollection interface [Windows Ribbon]","Add method","IUICollection.Add","IUICollection::Add","scenicintent_IUICollection_Add","uiribbon/IUICollection::Add","windowsribbon.windowsribbon_iuicollection_add"]
old-location: windowsribbon\windowsribbon_iuicollection_add.htm
tech.root: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuicollection\add.htm
ms.date: 12/05/2018
ms.keywords: Add, Add method [Windows Ribbon], Add method [Windows Ribbon],IUICollection interface, IUICollection interface [Windows Ribbon],Add method, IUICollection.Add, IUICollection::Add, scenicintent_IUICollection_Add, uiribbon/IUICollection::Add, windowsribbon.windowsribbon_iuicollection_add
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
 - IUICollection::Add
 - uiribbon/IUICollection::Add
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
 - IUICollection.Add
---

# IUICollection::Add


## -description

Adds an item to the end of the <a href="/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection">IUICollection</a>.

## -parameters

### -param item [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

Pointer to the item that is added to the <a href="/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection">IUICollection</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/windowsribbon/windowsribbon-gallerysample">Gallery Sample</a>



<a href="/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection">IUICollection</a>