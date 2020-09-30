---
UID: NS:wsdtypes._WSD_OPERATION
title: WSD_OPERATION (wsdtypes.h)
description: Describes an operation as defined by WSDL in terms of one or two messages.
helpviewer_keywords: ["WSD_OPERATION","WSD_OPERATION structure","ncd.wsd_operation_struct","wsdtypes/WSD_OPERATION"]
old-location: ncd\wsd_operation_struct.htm
tech.root: ncd
ms.assetid: fcd4895d-5357-4b73-90b9-e506e3d7f16e
ms.date: 12/05/2018
ms.keywords: WSD_OPERATION, WSD_OPERATION structure, ncd.wsd_operation_struct, wsdtypes/WSD_OPERATION
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
req.typenames: WSD_OPERATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSD_OPERATION
 - wsdtypes/_WSD_OPERATION
 - WSD_OPERATION
 - wsdtypes/WSD_OPERATION
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
 - WSD_OPERATION
---

# WSD_OPERATION structure


## -description

Describes an operation as defined by WSDL in terms of one or two messages. This structure is populated by <a href="/windows/desktop/WsdApi/web-services-for-devices-code-generator">generated code</a>.

## -struct-fields

### -field RequestType

Reference to a <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_type">WSDXML_TYPE</a> structure that specifies the request type of an incoming message.

### -field ResponseType

Reference to a <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_type">WSDXML_TYPE</a> structure that specifies the response type of an outgoing message.

### -field RequestStubFunction

Reference to a <a href="/windows/desktop/api/wsdtypes/nc-wsdtypes-wsd_stub_function">WSD_STUB_FUNCTION</a> function that specifies the address of a stub function which translates a generic SOAP message structure into a method call with a signature specific to the incoming message of the operation.