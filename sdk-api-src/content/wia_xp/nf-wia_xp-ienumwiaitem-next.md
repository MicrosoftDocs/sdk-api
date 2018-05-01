---
UID: NF:wia_xp.IEnumWiaItem.Next
title: IEnumWiaItem::Next method
author: windows-driver-content
description: The IEnumWiaItem::Next method fills an array of pointers to IWiaItem interfaces.
old-location: wia\_wia_IEnumWiaItem_Next.htm
old-project: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\ienumwiaitem\next.htm
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: IEnumWiaItem, IEnumWiaItem interface [WIA], Next method, IEnumWiaItem::Next, Next method [WIA], Next method [WIA], IEnumWiaItem interface, Next,IEnumWiaItem.Next, _wia_IEnumWiaItem_Next, wia._wia_IEnumWiaItem_Next, wia_xp/IEnumWiaItem::Next
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wia_xp.h
req.include-header: Wia.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WIAVIDEO_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wiaguid.lib
-	Wiaguid.dll
api_name:
-	IEnumWiaItem.Next
product: Windows
targetos: Windows
req.lib: Wiaguid.lib
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IEnumWiaItem::Next method


## -description


The <b>IEnumWiaItem::Next</b> method fills an array of pointers to <a href="https://msdn.microsoft.com/b9aaf7ae-7222-44d1-8cf1-89234b263135">IWiaItem</a> interfaces.


## -parameters




### -param celt [in]

Type: <b>ULONG</b>

Specifies the number of array elements in the array indicated by the <i>ppIWiaItem</i> parameter.


### -param ppIWiaItem [out]

Type: <b><a href="https://msdn.microsoft.com/b9aaf7ae-7222-44d1-8cf1-89234b263135">IWiaItem</a>**</b>

Receives the address of an array of <a href="https://msdn.microsoft.com/b9aaf7ae-7222-44d1-8cf1-89234b263135">IWiaItem</a> interface pointers. <b>IEnumWiaItem::Next</b> fills this array with interface pointers.


### -param pceltFetched [in, out]

Type: <b>ULONG*</b>

On output, this parameter receives the number of interface pointers actually stored in the array indicated by the <i>ppIWiaItem</i> parameter. When the enumeration is complete, this parameter will contain zero.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, the method returns S_OK. When the enumeration is complete, it returns S_FALSE. If the method fails, it returns a standard COM error code.




## -remarks



The Windows Image Acquisition (WIA) run-time system represents WIA hardware devices as a hierarchical tree of <a href="https://msdn.microsoft.com/b9aaf7ae-7222-44d1-8cf1-89234b263135">IWiaItem</a> objects. Applications use the <b>IEnumWiaItem::Next</b> method to obtain an <b>IWiaItem</b> interface pointer for each item in the current folder of a hardware device's <b>IWiaItem</b> object tree. 

To obtain the list of pointers, the application passes an array of <a href="https://msdn.microsoft.com/b9aaf7ae-7222-44d1-8cf1-89234b263135">IWiaItem</a> interface pointers that it allocates. It also passes the number of array elements in the <i>celt</i> parameter. The <b>IEnumWiaItem::Next</b> method fills the array with pointers to <b>IWiaItem</b> interfaces. 

Until the enumeration process completes, the <b>IEnumWiaItem::Next</b> method returns S_OK. Each time it does, it sets the value pointed to by <i>pceltFetched</i> to the number of items it inserted into the array. When <b>IEnumWiaItem::Next</b> finishes the process of enumerating <a href="https://msdn.microsoft.com/b9aaf7ae-7222-44d1-8cf1-89234b263135">IWiaItem</a> objects, it returns S_FALSE and sets the memory location pointed to by <i>pceltFetched</i> to zero.

Applications must call the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> method on the interface pointers they receive through the <i>ppIWiaItem</i> parameter.



