---
UID: NF:uiribbon.IUICollection.Insert
title: IUICollection::Insert
author: windows-driver-content
description: Inserts an item into the IUICollection at the specified index.
old-location: windowsribbon\windowsribbon_iuicollection_insert.htm
old-project: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuicollection\insert.htm
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: IUICollection interface [Windows Ribbon],Insert method, IUICollection.Insert, IUICollection::Insert, Insert, Insert method [Windows Ribbon], Insert method [Windows Ribbon],IUICollection interface, scenicintent_IUICollection_Insert, uiribbon/IUICollection::Insert, windowsribbon.windowsribbon_iuicollection_insert
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
req.typenames: UI_VIEWVERB
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mshtml.dll
api_name:
-	IUICollection.Insert
product: Windows
targetos: Windows
req.lib: 
req.dll: Mshtml.dll
req.irql: 
req.product: Windows UI
---

# IUICollection::Insert


## -description


Inserts an item into the <a href="https://msdn.microsoft.com/c239a724-9d7e-4204-933a-8e10581b4ecc">IUICollection</a> at the specified index.


## -parameters




### -param index [in]

Type: <b>UINT32</b>


					The zero-based index at which <i>item</i> is inserted into the <a href="https://msdn.microsoft.com/c239a724-9d7e-4204-933a-8e10581b4ecc">IUICollection</a>.
				


### -param item [in]

Type: <b><a href="_com_iunknown">IUnknown</a>*</b>


					Pointer to the item that is added to the <a href="https://msdn.microsoft.com/c239a724-9d7e-4204-933a-8e10581b4ecc">IUICollection</a>.
				


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1a462f4e-e75a-40cf-9c52-0bad0a645d57">Gallery Sample</a>



<a href="https://msdn.microsoft.com/c239a724-9d7e-4204-933a-8e10581b4ecc">IUICollection</a>
 

 

