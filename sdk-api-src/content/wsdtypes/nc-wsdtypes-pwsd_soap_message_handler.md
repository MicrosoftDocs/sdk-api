---
UID: NC:wsdtypes.PWSD_SOAP_MESSAGE_HANDLER
title: PWSD_SOAP_MESSAGE_HANDLER (wsdtypes.h)
description: References a SOAP message handler for incoming messages.
helpviewer_keywords: ["PWSD_SOAP_MESSAGE_HANDLER","PWSD_SOAP_MESSAGE_HANDLER callback","PWSD_SOAP_MESSAGE_HANDLER callback function","callback function pointer","ncd.pwsd_soap_message_handler_func","wsdtypes/PWSD_SOAP_MESSAGE_HANDLER"]
old-location: ncd\pwsd_soap_message_handler_func.htm
tech.root: ncd
ms.assetid: 175d4352-ba85-4c3c-be9f-4612c4b66123
ms.date: 12/05/2018
ms.keywords: PWSD_SOAP_MESSAGE_HANDLER, PWSD_SOAP_MESSAGE_HANDLER callback, PWSD_SOAP_MESSAGE_HANDLER callback function, callback function pointer, ncd.pwsd_soap_message_handler_func, wsdtypes/PWSD_SOAP_MESSAGE_HANDLER
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PWSD_SOAP_MESSAGE_HANDLER
 - wsdtypes/PWSD_SOAP_MESSAGE_HANDLER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Wsdtypes.h
api_name:
 - PWSD_SOAP_MESSAGE_HANDLER
---

# PWSD_SOAP_MESSAGE_HANDLER callback function


## -description

References a SOAP message handler for incoming messages. This is an internal function pointer, and it should not be used by WSDAPI clients or services.

## -parameters

### -param thisUnknown

Pointer to the object calling this function.

### -param event

A <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_event">WSD_EVENT</a> structure containing the message to be handled.

## -returns

Possible return values include, but are not limited to, the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
