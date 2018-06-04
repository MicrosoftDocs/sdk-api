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

# IWiaItem::CreateChildItem


## -description


The <b>IWiaItem::CreateChildItem</b> method is used by applications to add <a href="https://msdn.microsoft.com/b9aaf7ae-7222-44d1-8cf1-89234b263135">IWiaItem</a> objects to the <b>IWiaItem</b> tree of a device.


## -parameters




### -param lFlags [in]

Type: <b>LONG</b>

Specifies the WIA item type. Must be set to one of the values listed in <a href="https://msdn.microsoft.com/7961f692-088a-4f3b-84e9-5fabb0373c3c">WIA Item Type Flags</a>.


### -param bstrItemName [in]

Type: <b>BSTR</b>

Specifies the WIA item name, such as "Top". You can think of this parameter as being equivalent to a file name.



### -param bstrFullItemName [in]

Type: <b>BSTR</b>

Specifies the full WIA item name. You can think of this parameter as equivalent to a full path to a file, such as "003\Root\Top".


### -param ppIWiaItem [out]

Type: <b><a href="https://msdn.microsoft.com/b9aaf7ae-7222-44d1-8cf1-89234b263135">IWiaItem</a>**</b>

Receives the address of a pointer to the <a href="https://msdn.microsoft.com/b9aaf7ae-7222-44d1-8cf1-89234b263135">IWiaItem</a> interface that sets the <b>IWiaItem::CreateChildItem</b> method.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Some WIA hardware devices allow applications to create new items in the <a href="https://msdn.microsoft.com/b9aaf7ae-7222-44d1-8cf1-89234b263135">IWiaItem</a> tree that represents the device. Applications must test the devices to see if they support this capability. Use the <a href="https://msdn.microsoft.com/736a8aba-58e0-4b52-a997-ef1fb80473ba">IEnumWIA_DEV_CAPS</a> interface to enumerate the current device's capabilities.

If the device allows the creation of new items in the <a href="https://msdn.microsoft.com/b9aaf7ae-7222-44d1-8cf1-89234b263135">IWiaItem</a> tree, invoking <b>IWiaItem::CreateChildItem</b> creates a new <b>IWiaItem</b> that is a child of the current node. <b>IWiaItem::CreateChildItem</b> passes a pointer to the new node to the application through the <i>ppIWiaItem</i> parameter.

Applications must call the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> method on the interface pointers they receive through the <i>ppIWiaItem</i> parameter.



