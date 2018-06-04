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

# IWiaDevMgr::CreateDevice


## -description


The <b>IWiaDevMgr::CreateDevice</b> creates a hierarchical tree of <a href="https://msdn.microsoft.com/b9aaf7ae-7222-44d1-8cf1-89234b263135">IWiaItem</a> objects for a Windows Image Acquisition (WIA) device.


## -parameters




### -param bstrDeviceID [in]

Type: <b>BSTR</b>

Specifies the unique identifier of the WIA device.


### -param ppWiaItemRoot [out]

Type: <b><a href="https://msdn.microsoft.com/b9aaf7ae-7222-44d1-8cf1-89234b263135">IWiaItem</a>**</b>

Pointer to a pointer to the <a href="https://msdn.microsoft.com/b9aaf7ae-7222-44d1-8cf1-89234b263135">IWiaItem</a> interface of the root item in the hierarchical tree for the WIA device.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Applications use the <b>IWiaDevMgr::CreateDevice</b> method to create a device object for the WIA devices specified by the <i>bstrDeviceID</i> parameter. 

When it returns, the <b>IWiaDevMgr::CreateDevice</b> method stores an address of a pointer in the parameter <i>ppWiaItemRoot</i>. The pointer points to the root item of the tree of <a href="https://msdn.microsoft.com/b9aaf7ae-7222-44d1-8cf1-89234b263135">IWiaItem</a> objects created by <b>IWiaDevMgr::CreateDevice</b>. Applications can use this tree of objects to control and retrieve data from the WIA device.

Note that applications must call the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> method on the pointers they receive through the <i>ppWiaItemRoot</i> parameter.



