---
UID: NS:wsdtypes._WSD_SOAP_FAULT_SUBCODE
title: WSD_SOAP_FAULT_SUBCODE (wsdtypes.h)
description: Represents a generated SOAP fault subcode.
helpviewer_keywords: ["WSD_SOAP_FAULT_SUBCODE","WSD_SOAP_FAULT_SUBCODE structure","ncd.wsd_soap_fault_subcode_struct","wsdtypes/WSD_SOAP_FAULT_SUBCODE"]
old-location: ncd\wsd_soap_fault_subcode_struct.htm
tech.root: ncd
ms.assetid: cd8f35e4-7b22-4af0-b6a4-78f43ed8b060
ms.date: 12/05/2018
ms.keywords: WSD_SOAP_FAULT_SUBCODE, WSD_SOAP_FAULT_SUBCODE structure, ncd.wsd_soap_fault_subcode_struct, wsdtypes/WSD_SOAP_FAULT_SUBCODE
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
req.typenames: WSD_SOAP_FAULT_SUBCODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSD_SOAP_FAULT_SUBCODE
 - wsdtypes/_WSD_SOAP_FAULT_SUBCODE
 - WSD_SOAP_FAULT_SUBCODE
 - wsdtypes/WSD_SOAP_FAULT_SUBCODE
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
 - WSD_SOAP_FAULT_SUBCODE
---

# WSD_SOAP_FAULT_SUBCODE structure


## -description

Represents a generated SOAP fault subcode.  Subcodes can be nested.

## -struct-fields

### -field Value

A <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_name">WSDXML_NAME</a> structure that contains the  qualified name of the SOAP fault subcode.

### -field Subcode

A <b>WSD_SOAP_FAULT_SUBCODE</b> structure that contains a fault subcode.

## -see-also

<a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_soap_fault_code">WSD_SOAP_FAULT_CODE</a>