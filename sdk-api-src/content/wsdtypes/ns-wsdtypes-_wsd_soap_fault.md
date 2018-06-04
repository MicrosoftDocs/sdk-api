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

# _WSD_SOAP_FAULT structure


## -description


Represents a generated SOAP fault.


## -struct-fields




### -field Code

A <a href="https://msdn.microsoft.com/b71f4bcc-d125-4091-a491-1a5a2aea2310">WSD_SOAP_FAULT_CODE</a> structure that contains a SOAP fault code.


### -field Reason

A <a href="https://msdn.microsoft.com/c1b2ac44-8a86-4aac-a0d3-3b8d80a6b1d9">WSD_SOAP_FAULT_REASON</a> structure that contains localized human readable explanations of the fault.


### -field Node

The SOAP node on the SOAP message path that caused the fault.


### -field Role

The SOAP role in which the <b>Node</b> was acting at the time the fault occurred.


### -field Detail

A <a href="https://msdn.microsoft.com/727149b4-31b0-4fd8-b0fa-eb773edb171e">WSDXML_ELEMENT</a> structure that contains application-specific error information pertaining to the fault.


## -see-also




<a href="https://msdn.microsoft.com/eebecf71-2572-4e20-ad40-b1a2f811bedf">WSDGenerateFault</a>



<a href="https://msdn.microsoft.com/11cdd975-cc06-4fdc-8d84-c419e2a2b5ff">WSDGenerateFaultEx</a>
 

 

