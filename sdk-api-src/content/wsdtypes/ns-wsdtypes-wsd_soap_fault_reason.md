---
UID: NS:wsdtypes._WSD_SOAP_FAULT_REASON
title: WSD_SOAP_FAULT_REASON (wsdtypes.h)
description: A collection of reason codes associated with a WSD_SOAP_FAULT.
helpviewer_keywords: ["WSD_SOAP_FAULT_REASON","WSD_SOAP_FAULT_REASON structure","ncd.wsd_soap_fault_reason_struct","wsdtypes/WSD_SOAP_FAULT_REASON"]
old-location: ncd\wsd_soap_fault_reason_struct.htm
tech.root: ncd
ms.assetid: c1b2ac44-8a86-4aac-a0d3-3b8d80a6b1d9
ms.date: 12/05/2018
ms.keywords: WSD_SOAP_FAULT_REASON, WSD_SOAP_FAULT_REASON structure, ncd.wsd_soap_fault_reason_struct, wsdtypes/WSD_SOAP_FAULT_REASON
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
req.typenames: WSD_SOAP_FAULT_REASON
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSD_SOAP_FAULT_REASON
 - wsdtypes/_WSD_SOAP_FAULT_REASON
 - WSD_SOAP_FAULT_REASON
 - wsdtypes/WSD_SOAP_FAULT_REASON
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
 - WSD_SOAP_FAULT_REASON
---

# WSD_SOAP_FAULT_REASON structure


## -description

A collection of reason codes associated with a  <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_soap_fault">WSD_SOAP_FAULT</a>. A reason code is a human readable explanation of the fault.

## -struct-fields

### -field Text

A <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_localized_string_list">WSD_LOCALIZED_STRING_LIST</a> structure that contains a collection of localized reason codes.

## -see-also

<a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_soap_fault">WSD_SOAP_FAULT</a>