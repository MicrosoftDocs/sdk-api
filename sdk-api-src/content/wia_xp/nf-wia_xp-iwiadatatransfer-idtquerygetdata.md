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

# IWiaDataTransfer::idtQueryGetData


## -description


The <b>IWiaDataTransfer::idtQueryGetData</b> method is used by applications to query a Windows Image Acquisition (WIA) device to determine what types of data formats it supports.



## -parameters




### -param pfe [in]

Type: <b><a href="https://msdn.microsoft.com/1dcc138b-b8c0-4d3a-bd9d-f4f5522d91ea">WIA_FORMAT_INFO</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/1dcc138b-b8c0-4d3a-bd9d-f4f5522d91ea">WIA_FORMAT_INFO</a> structure.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns S_OK. Otherwise it returns a value specified in <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>, or a standard COM error.





## -remarks



This method queries a device to determine the data formats it supports. Prior to a data transfer, an application can fill in the <a href="https://msdn.microsoft.com/1dcc138b-b8c0-4d3a-bd9d-f4f5522d91ea">WIA_FORMAT_INFO</a> structure with the intended medium and data format information. It then calls <b>IWiaDataTransfer::idtQueryGetData</b> and receives a return value of S_OK if the data format and media type are supported by this device.



