---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IWiaItem::EnumChildItems


## -description


The <b>IWiaItem::EnumChildItems</b> method creates an enumerator object and passes back a pointer to its <a href="https://msdn.microsoft.com/25eab463-a531-4cb7-b8b7-6b1c8d060ee8">IEnumWiaItem</a> interface for non-empty folders in a <a href="https://msdn.microsoft.com/b9aaf7ae-7222-44d1-8cf1-89234b263135">IWiaItem</a> tree of a Windows Image Acquisition (WIA) device.


## -parameters




### -param ppIEnumWiaItem [out]

Type: <b><a href="https://msdn.microsoft.com/25eab463-a531-4cb7-b8b7-6b1c8d060ee8">IEnumWiaItem</a>**</b>

Receives the address of a pointer to the <a href="https://msdn.microsoft.com/25eab463-a531-4cb7-b8b7-6b1c8d060ee8">IEnumWiaItem</a> interface that <b>IWiaItem::EnumChildItems</b> creates.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The WIA run-time system represents each WIA hardware device as a hierarchical tree of <a href="https://msdn.microsoft.com/b9aaf7ae-7222-44d1-8cf1-89234b263135">IWiaItem</a> objects. The <b>IWiaItem::EnumChildItems</b> method enables applications to enumerate child items in the current item. However, it can only be applied to items that are folders. 

If the folder is not empty, it contains a subtree of <a href="https://msdn.microsoft.com/b9aaf7ae-7222-44d1-8cf1-89234b263135">IWiaItem</a> objects. The <b>IWiaItem::EnumChildItems</b> method enumerates all of the items contained in the folder. It stores a pointer to an enumerator in the <i>ppIEnumWiaItem</i> parameter. Applications use the enumerator pointer to perform the enumeration of an object's child items.

Applications must call the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> method on the interface pointers they receive through the <i>ppIEnumWiaItem</i> parameter.



