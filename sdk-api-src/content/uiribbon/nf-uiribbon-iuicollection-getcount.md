---
UID: NF:uiribbon.IUICollection.GetCount
title: IUICollection::GetCount (uiribbon.h)
description: Retrieves the number of items contained in the IUICollection.
helpviewer_keywords: ["GetCount","GetCount method [Windows Ribbon]","GetCount method [Windows Ribbon]","IUICollection interface","IUICollection interface [Windows Ribbon]","GetCount method","IUICollection.GetCount","IUICollection::GetCount","scenicintent_IUICollection_GetCount","uiribbon/IUICollection::GetCount","windowsribbon.windowsribbon_iuicollection_getcount"]
old-location: windowsribbon\windowsribbon_iuicollection_getcount.htm
tech.root: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuicollection\getcount.htm
ms.date: 12/05/2018
ms.keywords: GetCount, GetCount method [Windows Ribbon], GetCount method [Windows Ribbon],IUICollection interface, IUICollection interface [Windows Ribbon],GetCount method, IUICollection.GetCount, IUICollection::GetCount, scenicintent_IUICollection_GetCount, uiribbon/IUICollection::GetCount, windowsribbon.windowsribbon_iuicollection_getcount
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
 - IUICollection::GetCount
 - uiribbon/IUICollection::GetCount
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
 - IUICollection.GetCount
---

# IUICollection::GetCount


## -description

Retrieves the number of items contained in the <a href="/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection">IUICollection</a>.

## -parameters

### -param count [out]

Type: <b>UINT32*</b>

When this method returns, contains the item count.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/windowsribbon/windowsribbon-gallerysample">Gallery Sample</a>



<a href="/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection">IUICollection</a>