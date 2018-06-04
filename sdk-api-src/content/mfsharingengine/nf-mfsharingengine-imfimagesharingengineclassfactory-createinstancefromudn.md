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

# IMFImageSharingEngineClassFactory::CreateInstanceFromUDN


## -description


Creates an instance of the <a href="https://msdn.microsoft.com/A30C73DA-9BD5-4D12-A6FB-771BBD2D1191">IMFImageSharingEngine</a> from the provided unique device name.


## -parameters




### -param pUniqueDeviceName

The unique device name of the device with which the sharing engine is created.


### -param ppEngine [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/A30C73DA-9BD5-4D12-A6FB-771BBD2D1191">IMFImageSharingEngine</a> interface. The caller must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/7D6385BC-4D9C-4026-9363-0F6917A62BDE">IMFImageSharingEngineClassFactory</a>
 

 

