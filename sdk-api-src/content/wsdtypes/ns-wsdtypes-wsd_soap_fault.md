---
UID: NS:wsdtypes._WSD_SOAP_FAULT
title: WSD_SOAP_FAULT (wsdtypes.h)
description: Represents a generated SOAP fault.
helpviewer_keywords: ["WSD_SOAP_FAULT","WSD_SOAP_FAULT structure","ncd.wsd_soap_fault_struct","wsdtypes/WSD_SOAP_FAULT"]
old-location: ncd\wsd_soap_fault_struct.htm
tech.root: ncd
ms.assetid: ed5e2575-203a-41a2-b656-50cb82aae088
ms.date: 12/05/2018
ms.keywords: WSD_SOAP_FAULT, WSD_SOAP_FAULT structure, ncd.wsd_soap_fault_struct, wsdtypes/WSD_SOAP_FAULT
req.header: wsdtypes.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WSD_SOAP_FAULT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSD_SOAP_FAULT
 - wsdtypes/_WSD_SOAP_FAULT
 - WSD_SOAP_FAULT
 - wsdtypes/WSD_SOAP_FAULT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WsdTypes.h
api_name:
 - WSD_SOAP_FAULT
---

# WSD_SOAP_FAULT structure


## -description

Represents a generated SOAP fault.

## -struct-fields

### -field Code

A <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_soap_fault_code">WSD_SOAP_FAULT_CODE</a> structure that contains a SOAP fault code.

### -field Reason

A <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_soap_fault_reason">WSD_SOAP_FAULT_REASON</a> structure that contains localized human readable explanations of the fault.

### -field Node

The SOAP node on the SOAP message path that caused the fault.

### -field Role

The SOAP role in which the <b>Node</b> was acting at the time the fault occurred.

### -field Detail

A <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_element">WSDXML_ELEMENT</a> structure that contains application-specific error information pertaining to the fault.

## -see-also

<a href="/windows/desktop/api/wsdutil/nf-wsdutil-wsdgeneratefault">WSDGenerateFault</a>



<a href="/windows/desktop/api/wsdutil/nf-wsdutil-wsdgeneratefaultex">WSDGenerateFaultEx</a>