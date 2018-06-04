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

# IBDA_GuideDataDeliveryService::GetServiceInfoFromTuneXml


## -description


Gets service information from an XML tune request.


## -parameters




### -param bstrTuneXml [in]

The XML tune request. For more information, see <a href="https://msdn.microsoft.com/5f429473-6a48-4298-b8f4-61809604ffbd">IBDA_GuideDataDeliveryService::GetTuneXmlFromServiceIdx</a> or the section on tuning schemas in Part 1 of the Protected Broadcast Driver Architecture (PBDA) specification, which can be downloaded from <a href="http://go.microsoft.com/fwlink/p/?linkid=132926">http://go.microsoft.com/fwlink/p/?linkid=132926</a>.


### -param pbstrServiceDescription [out]

Receives an XML string that contains information about the service. The caller must release the string by calling <b>SysFreeString</b>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5329f725-e77e-49c2-87f5-f7204d022adc">IBDA_GuideDataDeliveryService</a>
 

 

