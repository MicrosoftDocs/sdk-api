---
UID: NC:wsdtypes.PWSD_SOAP_MESSAGE_HANDLER
title: PWSD_SOAP_MESSAGE_HANDLER
author: windows-driver-content
description: References a SOAP message handler for incoming messages.
old-location: ncd\pwsd_soap_message_handler_func.htm
old-project: WsdApi
ms.assetid: 175d4352-ba85-4c3c-be9f-4612c4b66123
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: PWSD_SOAP_MESSAGE_HANDLER, PWSD_SOAP_MESSAGE_HANDLER function pointer, ncd.pwsd_soap_message_handler_func, wsdtypes/PWSD_SOAP_MESSAGE_HANDLER
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
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
req.typenames: WSD_SECURITY_SIGNATURE_VALIDATION, *PWSD_SECURITY_SIGNATURE_VALIDATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Wsdtypes.h
api_name:
-	PWSD_SOAP_MESSAGE_HANDLER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# PWSD_SOAP_MESSAGE_HANDLER callback


## -description


References a SOAP message handler for incoming messages. This is an internal function pointer, and it should not be used by WSDAPI clients or services.


## -parameters




### -param *thisUnknown

Pointer to the object calling this function.


### -param *event

A <a href="https://msdn.microsoft.com/d8697474-bfe5-4704-b1ac-15cf96f2ca92">WSD_EVENT</a> structure containing the message to be handled.


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
 



