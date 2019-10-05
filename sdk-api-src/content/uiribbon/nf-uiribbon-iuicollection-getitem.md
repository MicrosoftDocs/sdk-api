---
UID: NF:uiribbon.IUICollection.GetItem
title: IUICollection::GetItem (uiribbon.h)
author: windows-sdk-content
description: Retrieves an item from the IUICollection at the specified index.
old-location: windowsribbon\windowsribbon_iuicollection_getitem.htm
tech.root: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuicollection\getitem.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetItem, GetItem method [Windows Ribbon], GetItem method [Windows Ribbon],IUICollection interface, IUICollection interface [Windows Ribbon],GetItem method, IUICollection.GetItem, IUICollection::GetItem, scenicintent_IUICollection_GetItem, uiribbon/IUICollection::GetItem, windowsribbon.windowsribbon_iuicollection_getitem
ms.topic: method
f1_keywords: 
 - "uiribbon/IUICollection.GetItem"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mshtml.dll
api_name:
 - IUICollection.GetItem
targetos: Windows
req.typenames: 
req.redist: 
req.product: Windows UI
ms.custom: 19H1
---

# IUICollection::GetItem


## -description


Retrieves an item from the <a href="https://docs.microsoft.com/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection">IUICollection</a> at the specified index.


## -parameters




### -param index [in]

Type: <b>UINT32</b>

The zero-based index of <i>item</i> to retrieve from the <a href="https://docs.microsoft.com/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection">IUICollection</a>.
				


### -param item [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>**</b>

When this method returns, contains the address of a pointer variable that receives the item.
				


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/windowsribbon/windowsribbon-gallerysample">Gallery Sample</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection">IUICollection</a>
 

 

