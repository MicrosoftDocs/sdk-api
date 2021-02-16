---
UID: NS:wsdtypes._WSD_SOAP_FAULT_CODE
title: WSD_SOAP_FAULT_CODE (wsdtypes.h)
description: Represents a generated SOAP fault code.
helpviewer_keywords: ["WSD_SOAP_FAULT_CODE","WSD_SOAP_FAULT_CODE structure","ncd.wsd_soap_fault_code_struct","wsdtypes/WSD_SOAP_FAULT_CODE"]
old-location: ncd\wsd_soap_fault_code_struct.htm
tech.root: ncd
ms.assetid: b71f4bcc-d125-4091-a491-1a5a2aea2310
ms.date: 12/05/2018
ms.keywords: WSD_SOAP_FAULT_CODE, WSD_SOAP_FAULT_CODE structure, ncd.wsd_soap_fault_code_struct, wsdtypes/WSD_SOAP_FAULT_CODE
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
req.typenames: WSD_SOAP_FAULT_CODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSD_SOAP_FAULT_CODE
 - wsdtypes/_WSD_SOAP_FAULT_CODE
 - WSD_SOAP_FAULT_CODE
 - wsdtypes/WSD_SOAP_FAULT_CODE
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
 - WSD_SOAP_FAULT_CODE
---

# WSD_SOAP_FAULT_CODE structure


## -description

Represents a generated SOAP fault code.

## -struct-fields

### -field Value

A <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_name">WSDXML_NAME</a> structure that contains the  qualified name of the SOAP fault code.

### -field Subcode

A <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_soap_fault_subcode">WSD_SOAP_FAULT_SUBCODE</a> structure that contains the fault subcode.

## -see-also

<a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_soap_fault">WSD_SOAP_FAULT</a>