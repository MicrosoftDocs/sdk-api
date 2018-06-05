---
UID: NS:wsdtypes._WSD_SOAP_FAULT
title: "_WSD_SOAP_FAULT"
author: windows-sdk-content
description: Represents a generated SOAP fault.
old-location: ncd\wsd_soap_fault_struct.htm
old-project: WsdApi
ms.assetid: ed5e2575-203a-41a2-b656-50cb82aae088
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: WSD_SOAP_FAULT, WSD_SOAP_FAULT structure, _WSD_SOAP_FAULT, ncd.wsd_soap_fault_struct, wsdtypes/WSD_SOAP_FAULT
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wsdtypes.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wsdhost.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WSD_SOAP_FAULT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WsdTypes.h
api_name:
-	WSD_SOAP_FAULT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
 

 

