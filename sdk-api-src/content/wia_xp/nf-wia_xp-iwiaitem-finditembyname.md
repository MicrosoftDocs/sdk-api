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



