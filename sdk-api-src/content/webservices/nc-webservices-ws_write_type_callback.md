---
UID: NC:webservices.WS_WRITE_TYPE_CALLBACK
title: WS_WRITE_TYPE_CALLBACK
author: windows-driver-content
description: Invoked to write an element when WS_CUSTOM_TYPE has been specified.
old-location: wsw\ws_write_type_callback.htm
old-project: wsw
ms.assetid: f94bdf80-abea-4a97-9d41-add498e314b1
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: WS_WRITE_TYPE_CALLBACK, WS_WRITE_TYPE_CALLBACK callback function [Web Services for Windows], webservices/WS_WRITE_TYPE_CALLBACK, wsw.ws_write_type_callback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WDSTRANSPORT_TFTP_CAPABILITY, *PWDSTRANSPORT_TFTP_CAPABILITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	WebServices.h
api_name:
-	WS_WRITE_TYPE_CALLBACK
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WS_WRITE_TYPE_CALLBACK callback


## -description


Invoked to write an element when <a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_CUSTOM_TYPE</a>
                has been specified.  This allows writing of XML constructs which do not easily
                map to the core serialization model.
            


## -parameters




### -param *writer [in]

A  <b>WS_XML_WRITER</b> pointer to the writer that the value should be written to.
                


### -param typeMapping [in]

Indicates how the XML is being mapped to this type.  See <a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_TYPE_MAPPING</a>
                    for more information.
                


                    If a mapping does not make sense for this particular type, the callback
                    should return <b>WS_E_INVALID_OPERATION</b>. (See <a href="https://msdn.microsoft.com/96285557-8317-4875-b634-e2eacd605901">Windows Web Services Return Values</a>.)  A callback implementation
                    should be prepared to be passed new mapping types in future versions and should return
                    <b>WS_E_INVALID_OPERATION</b> for those cases.
                


### -param *descriptionData [in]


                    This is the value of the <b>descriptionData</b> field of the <a href="https://msdn.microsoft.com/7ae3d16c-0755-4226-844e-52cf96fa84fb">WS_CUSTOM_TYPE_DESCRIPTION</a> structure.
                    The callback uses this field to access any additional information about the type.
                


### -param *value

A  <b>void</b> pointer to a value to serialize.
                


### -param valueSize [in]

The size, in bytes, of the value being serialized.
                


### -param *error [in, optional]


                    A pointer to a <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> data structure where additional error information should be stored if the function fails.
                


## -returns



This callback function does not return a value.




## -remarks




                The callback will be invoked with the same calling sequence as
                <a href="https://msdn.microsoft.com/cab1b4d6-c18b-4740-b4a4-61e70ea181d9">WsWriteType</a> in the documentation for <a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_TYPE_MAPPING</a>.
                This defines what parts of the XML that the callback should write.
            



