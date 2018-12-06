---
UID: NF:uiribbon.IUICollection.GetItem
title: IUICollection::GetItem
author: windows-sdk-content
description: Retrieves an item from the IUICollection at the specified index.
old-location: windowsribbon\windowsribbon_iuicollection_getitem.htm
tech.root: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuicollection\getitem.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetItem, GetItem method [Windows Ribbon], GetItem method [Windows Ribbon],IUICollection interface, IUICollection interface [Windows Ribbon],GetItem method, IUICollection.GetItem, IUICollection::GetItem, scenicintent_IUICollection_GetItem, uiribbon/IUICollection::GetItem, windowsribbon.windowsribbon_iuicollection_getitem
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Windows UI
---

# IUICollection::GetItem


## -description


Retrieves an item from the <a href="https://msdn.microsoft.com/c239a724-9d7e-4204-933a-8e10581b4ecc">IUICollection</a> at the specified index.


## -parameters




### -param index [in]

Type: <b>UINT32</b>

The zero-based index of <i>item</i> to retrieve from the <a href="https://msdn.microsoft.com/c239a724-9d7e-4204-933a-8e10581b4ecc">IUICollection</a>.
				


### -param item [out]

Type: <b><a href="_com_iunknown">IUnknown</a>**</b>

When this method returns, contains the address of a pointer variable that receives the item.
				


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1a462f4e-e75a-40cf-9c52-0bad0a645d57">Gallery Sample</a>



<a href="https://msdn.microsoft.com/c239a724-9d7e-4204-933a-8e10581b4ecc">IUICollection</a>
 

 

