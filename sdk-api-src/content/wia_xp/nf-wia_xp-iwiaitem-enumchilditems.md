---
UID: NF:wia_xp.IWiaItem.EnumChildItems
title: IWiaItem::EnumChildItems
author: windows-sdk-content
description: The IWiaItem::EnumChildItems method creates an enumerator object and passes back a pointer to its IEnumWiaItem interface for non-empty folders in a IWiaItem tree of a Windows Image Acquisition (WIA) device.
old-location: wia\_wia_IWiaItem_EnumChildItems.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiaitem\enumchilditems.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: EnumChildItems, EnumChildItems method [WIA], EnumChildItems method [WIA],IWiaItem interface, IWiaItem interface [WIA],EnumChildItems method, IWiaItem.EnumChildItems, IWiaItem::EnumChildItems, _wia_IWiaItem_EnumChildItems, wia._wia_IWiaItem_EnumChildItems, wia_xp/IWiaItem::EnumChildItems
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
 - IWiaItem.EnumChildItems
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWiaItem::EnumChildItems


## -description


The <b>IWiaItem::EnumChildItems</b> method creates an enumerator object and passes back a pointer to its <a href="https://msdn.microsoft.com/en-us/library/ms630176(v=VS.85).aspx">IEnumWiaItem</a> interface for non-empty folders in a <a href="https://msdn.microsoft.com/en-us/library/ms630113(v=VS.85).aspx">IWiaItem</a> tree of a Windows Image Acquisition (WIA) device.


## -parameters




### -param ppIEnumWiaItem [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms630176(v=VS.85).aspx">IEnumWiaItem</a>**</b>

Receives the address of a pointer to the <a href="https://msdn.microsoft.com/en-us/library/ms630176(v=VS.85).aspx">IEnumWiaItem</a> interface that <b>IWiaItem::EnumChildItems</b> creates.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The WIA run-time system represents each WIA hardware device as a hierarchical tree of <a href="https://msdn.microsoft.com/en-us/library/ms630113(v=VS.85).aspx">IWiaItem</a> objects. The <b>IWiaItem::EnumChildItems</b> method enables applications to enumerate child items in the current item. However, it can only be applied to items that are folders. 

If the folder is not empty, it contains a subtree of <a href="https://msdn.microsoft.com/en-us/library/ms630113(v=VS.85).aspx">IWiaItem</a> objects. The <b>IWiaItem::EnumChildItems</b> method enumerates all of the items contained in the folder. It stores a pointer to an enumerator in the <i>ppIEnumWiaItem</i> parameter. Applications use the enumerator pointer to perform the enumeration of an object's child items.

Applications must call the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> method on the interface pointers they receive through the <i>ppIEnumWiaItem</i> parameter.



