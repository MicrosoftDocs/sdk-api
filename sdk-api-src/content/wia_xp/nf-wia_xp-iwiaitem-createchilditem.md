---
UID: NF:wia_xp.IWiaItem.CreateChildItem
title: IWiaItem::CreateChildItem
author: windows-sdk-content
description: The IWiaItem::CreateChildItem method is used by applications to add IWiaItem objects to the IWiaItem tree of a device.
old-location: wia\_wia_IWiaItem_CreateChildItem.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiaitem\createchilditem.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CreateChildItem, CreateChildItem method [WIA], CreateChildItem method [WIA],IWiaItem interface, IWiaItem interface [WIA],CreateChildItem method, IWiaItem.CreateChildItem, IWiaItem::CreateChildItem, _wia_IWiaItem_CreateChildItem, wia._wia_IWiaItem_CreateChildItem, wia_xp/IWiaItem::CreateChildItem
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
req.lib: Wiaguid.lib
req.dll: Wiaservc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wiaservc.dll
api_name:
 - IWiaItem.CreateChildItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



