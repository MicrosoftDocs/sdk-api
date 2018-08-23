---
UID: NF:wia_xp.IWiaItem.GetItemType
title: IWiaItem::GetItemType
author: windows-sdk-content
description: The IWiaItem::GetItemType method is called by applications to obtain the type information of an item.
old-location: wia\_wia_IWiaItem_GetItemType.htm
old-project: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiaitem\getitemtype.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetItemType, GetItemType method [WIA], GetItemType method [WIA],IWiaItem interface, IWiaItem interface [WIA],GetItemType method, IWiaItem.GetItemType, IWiaItem::GetItemType, _wia_IWiaItem_GetItemType, wia._wia_IWiaItem_GetItemType, wia_xp/IWiaItem::GetItemType
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wia_xp.h
req.include-header: Wia.h
req.redist: 
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
tech.root: 
req.typenames: WIAVIDEO_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wiaservc.dll
api_name:
 - IWiaItem.GetItemType
product: Windows
targetos: Windows
req.lib: Wiaguid.lib
req.dll: Wiaservc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWiaItem::GetItemType


## -description


The <b>IWiaItem::GetItemType</b> method is called by applications to obtain the type information of an item.


## -parameters




### -param pItemType [out]

Type: <b>LONG*</b>

Receives the address of a <b>LONG</b> variable that contains a combination of <a href="https://msdn.microsoft.com/7961f692-088a-4f3b-84e9-5fabb0373c3c">WIA Item Type Flags</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Every <a href="https://msdn.microsoft.com/b9aaf7ae-7222-44d1-8cf1-89234b263135">IWiaItem</a> object in the hierarchical tree of objects associated with a Windows Image Acquisition (WIA) hardware device has a specific data type. Item objects represent folders and files. Folders contain file objects. File objects contain data acquired by the device such as images and sounds. This method enables applications to identify the type of any item in a hierarchical tree of item objects in a device.

An item may have more than one type. For example, an item that represents an audio file will have the type attributes <a href="https://msdn.microsoft.com/7961f692-088a-4f3b-84e9-5fabb0373c3c">WiaItemTypeAudio</a> | <b>WiaItemTypeFile</b>.



