---
UID: NC:webservices.WS_READ_TYPE_CALLBACK
title: WS_READ_TYPE_CALLBACK
author: windows-sdk-content
description: Reads a value when WS_TYPEhas been specified.
old-location: wsw\ws_read_type_callback.htm
tech.root: wsw
ms.assetid: 95df152c-69cb-4417-9e85-e7ecb54ed042
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WS_READ_TYPE_CALLBACK, WS_READ_TYPE_CALLBACK callback, WS_READ_TYPE_CALLBACK callback function [Web Services for Windows], webservices/WS_READ_TYPE_CALLBACK, wsw.ws_read_type_callback
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - WebServices.h
api_name:
 - WS_READ_TYPE_CALLBACK
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WS_READ_TYPE_CALLBACK callback function


## -description


Reads a value when <a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_TYPE</a>has been specified.  This allows reading of XML constructs which do not easily
                map to the core serialization model.
            


## -parameters




### -param *reader [in]

A pointer to a <a href="https://msdn.microsoft.com/7acbe407-e91b-435a-82bc-acbbc13cfcfd">WS_XML_READER</a> handle that contains the type value.
                


### -param typeMapping [in]

Indicates how the XML is being mapped to this type.  

If a mapping does not make sense for this particular type, then the callback
                    should return <b>WS_E_INVALID_OPERATION</b>.  (See <a href="https://msdn.microsoft.com/96285557-8317-4875-b634-e2eacd605901">Windows Web Services Return Values</a>.) A callback implementation
                    should be prepared to be passed new mapping types in future versions and should return
                    <b>WS_E_INVALID_OPERATION</b> for those cases.
                


### -param *descriptionData [in]

 A pointer to the value of the <b>descriptionData</b> field of a  <a href="https://msdn.microsoft.com/7ae3d16c-0755-4226-844e-52cf96fa84fb">WS_CUSTOM_TYPE_DESCRIPTION</a> structure.
                    The callback can use this to gain access to any additional information about the type.
                


### -param *heap [in, optional]

A pointer to the heap for use in allocating any additional data associated with this type such as its nested fields.  
                

Note that this parameter may be <b>NULL</b>,
                    if the caller did not specify a <a href="https://msdn.microsoft.com/1866f54f-26fc-4889-a88f-0d298a418bdc">WS_HEAP</a> object when deserializing
                    the type.
                


### -param *value

A pointer to a buffer that holds the value that is being deserialized.
                    The callback is responsible for filling in the value based on the current 
                    contents of the reader and the typeMapping.
                    The callback can use the supplied heap if necessary to allocate
                    values associated with the value.
                


### -param valueSize [in]

The buffer size that is being deserialized.
                    The buffer is allocated according to the size specified in the
                    <a href="https://msdn.microsoft.com/7ae3d16c-0755-4226-844e-52cf96fa84fb">WS_CUSTOM_TYPE_DESCRIPTION</a>. 
                


### -param *error [in, optional]

A pointer to <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> data structure where additional error information should be stored if the function fails.
        


## -returns



This callback function does not return a value.




## -remarks



The callback will be invoked with the same calling sequence as
                <a href="https://msdn.microsoft.com/6d026b2e-f2c2-4990-9178-152585a7749a">WsReadType</a> in the documentation for <a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_TYPE_MAPPING</a>.
                This defines what parts of the XML that the callback should read.
            



