---
UID: NF:wia_xp.IWiaItem.FindItemByName
title: IWiaItem::FindItemByName
author: windows-sdk-content
description: The IWiaItem::FindItemByName method searches an item's tree of sub-items using the name as the search key. Each IWiaItem object has a name as one of its standard properties.
old-location: wia\_wia_IWiaItem_FindItemByName.htm
old-project: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiaitem\finditembyname.htm
ms.author: windowssdkdev
ms.date: 05/03/2018
ms.keywords: FindItemByName, FindItemByName method [WIA], FindItemByName method [WIA],IWiaItem interface, IWiaItem interface [WIA],FindItemByName method, IWiaItem.FindItemByName, IWiaItem::FindItemByName, _wia_IWiaItem_FindItemByName, wia._wia_IWiaItem_FindItemByName, wia_xp/IWiaItem::FindItemByName
ms.prod: windows
ms.technology: windows-sdk
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
 - IWiaItem.FindItemByName
product: Windows
targetos: Windows
req.lib: Wiaguid.lib
req.dll: Wiaservc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWiaItem::FindItemByName


## -description


The <b>IWiaItem::FindItemByName</b> method searches an item's tree of sub-items using the name as the search key. Each <a href="https://msdn.microsoft.com/b9aaf7ae-7222-44d1-8cf1-89234b263135">IWiaItem</a> object has a name as one of its standard properties.


## -parameters




### -param lFlags [in]

Type: <b>LONG</b>

Currently unused. Should be set to zero.


### -param bstrFullItemName [in]

Type: <b>BSTR</b>

Specifies the name of the item for which to search.


### -param ppIWiaItem [out]

Type: <b><a href="https://msdn.microsoft.com/b9aaf7ae-7222-44d1-8cf1-89234b263135">IWiaItem</a>**</b>

Pointer to the <a href="https://msdn.microsoft.com/b9aaf7ae-7222-44d1-8cf1-89234b263135">IWiaItem</a> interface.


## -returns



Type: <b>HRESULT</b>

This method returns S_OK if it finds the item, or S_FALSE if it does not find the item. If the method fails, it returns a standard COM error code.




## -remarks



This method searches the current item's tree of sub-items using the name as the search key. If <b>IWiaItem::FindItemByName</b> finds the item specified by <i>bstrFullItemName</i>, it stores the address of a pointer to the <a href="https://msdn.microsoft.com/b9aaf7ae-7222-44d1-8cf1-89234b263135">IWiaItem</a> interface of the item in the <i>ppIWiaItem</i> parameter.

Applications must call the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> method on the interface pointers they receive through the <i>ppIWiaItem</i> parameter.



