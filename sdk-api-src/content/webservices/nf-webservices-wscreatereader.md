---
UID: NF:webservices.WsCreateReader
title: WsCreateReader function (webservices.h)
author: windows-sdk-content
description: Creates an XML reader with the specified properties.
old-location: wsw\wscreatereader.htm
tech.root: wsw
ms.assetid: 0d4449aa-ffcc-41d9-99b1-7352edaf3700
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WsCreateReader, WsCreateReader function [Web Services for Windows], webservices/WsCreateReader, wsw.wscreatereader
ms.topic: function
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsCreateReader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WsCreateReader function


## -description



Creates an <a href="https://msdn.microsoft.com/1f99e45c-64ba-42fb-9bf0-35e27f1c5ef2">XML reader</a> with the specified properties.  




## -parameters




### -param properties

An array of <a href="https://msdn.microsoft.com/8864d679-c321-45bb-b774-f05696d6098e">WS_XML_READER_PROPERTY</a> structures containing optional properties for the XML reader.

The value of this parameter may be <b>NULL</b>, in which case, the <i>propertyCount</i> parameter must be 0 (zero).
                

For the properties that tiy can use to configure the XML reader.
        see the <a href="https://msdn.microsoft.com/b8d36716-e25a-4215-8bc7-30091b68c0f6">WS_XML_READER_PROPERTY_ID</a> enumeration. 
      


### -param propertyCount [in]

The number of properties in the <i>properties</i> array.
                


### -param reader

On   success, a pointer that receives the address of the  <a href="https://msdn.microsoft.com/7acbe407-e91b-435a-82bc-acbbc13cfcfd">WS_XML_READER</a> structure representing the new XML reader.
                
                When you no longer need this structure, you must free it by calling <a href="https://msdn.microsoft.com/31163bea-266f-43a3-bdf5-61386ebc197c">WsFreeReader</a>.


### -param error [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> structure  that receives additional error information if the function fails.
                
                


## -returns



If the function succeeds, it returns NO_ERROR; otherwise, it returns an HRESULT error code.




## -remarks



Use <a href="https://msdn.microsoft.com/d7ac5233-266e-4ca1-aa58-e50b385b48bb">WsSetInput</a> or <a href="https://msdn.microsoft.com/0b3ac6ab-8c16-4189-950d-84bdcdabcde0">WsSetInputToBuffer</a>functions to choose the encoding for the XML reader and to indicate the source of the input.
      

If <a href="https://msdn.microsoft.com/2a5ebe4a-e97d-4744-9ec9-da6da892e4c5">WS_READ_CALLBACK</a> is specified in the <a href="https://msdn.microsoft.com/1e7a708d-5dcf-44ec-b781-a34946cb2844">WS_XML_READER_INPUT</a> structure passed to the <a href="https://msdn.microsoft.com/d7ac5233-266e-4ca1-aa58-e50b385b48bb">WsSetInput</a> function, the XML reader reads
        additional data only when <a href="https://msdn.microsoft.com/1f4138a2-acc5-4f1d-8e35-544859d2fa49">WsFillReader</a> is called.  This allows the caller to determine
        at what granularity to read data and whether to read that data asynchronously.
      

A <a href="https://msdn.microsoft.com/7acbe407-e91b-435a-82bc-acbbc13cfcfd">WS_XML_READER</a> structure can be reused by calling <a href="https://msdn.microsoft.com/d7ac5233-266e-4ca1-aa58-e50b385b48bb">WsSetInput</a> or <a href="https://msdn.microsoft.com/0b3ac6ab-8c16-4189-950d-84bdcdabcde0">WsSetInputToBuffer</a> again.
      

If any API operation that operates on an <a href="https://msdn.microsoft.com/7acbe407-e91b-435a-82bc-acbbc13cfcfd">WS_XML_READER</a> fails the XML reader is left in a faulted state
        and further function calls return <b>WS_E_OBJECT_FAULTED</b>.  (See <a href="https://msdn.microsoft.com/96285557-8317-4875-b634-e2eacd605901">Windows Web Services Return Values</a>.) The only possible function calls for the XML reader
        if this occurs are <a href="https://msdn.microsoft.com/d7ac5233-266e-4ca1-aa58-e50b385b48bb">WsSetInput</a> and <a href="https://msdn.microsoft.com/0b3ac6ab-8c16-4189-950d-84bdcdabcde0">WsSetInputToBuffer</a> for returning the XML reader to a usable state,
        or <a href="https://msdn.microsoft.com/31163bea-266f-43a3-bdf5-61386ebc197c">WsFreeReader</a> for releasing the XML reader object.
      



