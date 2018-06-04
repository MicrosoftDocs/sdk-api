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

# IFaxInboundRoutingExtensions::get_Item


## -description


The <b>IFaxInboundRoutingExtensions::get_Item</b> method returns a <a href="https://msdn.microsoft.com/e967c113-a4c0-4a83-949b-eb51fe41fb42">IFaxInboundRoutingExtension</a> interface from the <a href="https://msdn.microsoft.com/6daf0614-c0d4-42ba-96de-60f35a39aff1">IFaxInboundRoutingExtensions</a> collection.


## -parameters




### -param vIndex [in]

Type: <b>VARIANT</b>

<b>VARIANT</b> that specifies the item to retrieve from the collection. 

                    

If this parameter is type VT_I2 or VT_I4, the parameter specifies the index of the item to retrieve from the collection. The index is 1-based. If this parameter is type VT_BSTR, the parameter is a string containing the unique name of the fax routing extension to retrieve. Other types are not supported.


### -param pFaxInboundRoutingExtension






#### - ppFaxInboundRoutingExtension [out, retval]

Type: <b><a href="https://msdn.microsoft.com/e967c113-a4c0-4a83-949b-eb51fe41fb42">IFaxInboundRoutingExtension</a>**</b>

Address of a pointer to an <a href="https://msdn.microsoft.com/e967c113-a4c0-4a83-949b-eb51fe41fb42">IFaxInboundRoutingExtension</a> interface.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6daf0614-c0d4-42ba-96de-60f35a39aff1">IFaxInboundRoutingExtensions</a>



<a href="https://msdn.microsoft.com/cef24608-cab1-4090-aa94-3a1b76733e98">Visual Basic Example</a>
 

 

