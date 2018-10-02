---
UID: NF:webservices.WsCreateWriter
title: WsCreateWriter function
author: windows-sdk-content
description: creates an XML Writer with the specified properties.
old-location: wsw\wscreatewriter.htm
tech.root: wsw
ms.assetid: 5b4bb009-764e-4892-903a-5939f5570016
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WsCreateWriter, WsCreateWriter function [Web Services for Windows], webservices/WsCreateWriter, wsw.wscreatewriter
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - WsCreateWriter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WsCreateWriter function


## -description



creates an <a href="https://msdn.microsoft.com/69d50793-1d5b-4fc7-bf69-128f8e23a98d">XML Writer</a> with the specified properties. 




## -parameters




### -param properties

An array of <a href="https://msdn.microsoft.com/2979d038-f0a8-407d-bf8e-dca4027f6410">WS_XML_WRITER_PROPERTY</a> structures containing optional properties for the XML writer.

The value of this parameter may be <b>NULL</b>, in which case, the <i>propertyCount</i> parameter must be 0 (zero).
                


### -param propertyCount [in]

The number of properties in the <i>properties</i> array.
                


### -param writer

On   success, a pointer that receives the address of the  <a href="https://msdn.microsoft.com/8f413e60-8a30-492c-8f2d-80be511fee11">WS_XML_WRITER</a> structure representing the created XML writer.
                
                When you no longer need this structure, you must free it by calling <a href="https://msdn.microsoft.com/eb1eb835-838a-41e4-9e7d-c5c805237f65">WsFreeWriter</a>.


### -param error [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> structure  that receives additional error information if the function fails.
                
                


## -returns



If the function succeeds, it returns NO_ERROR; otherwise, it returns an HRESULT error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more arguments are invalid.

</td>
</tr>
</table>
 




## -remarks



Use the <a href="https://msdn.microsoft.com/f0b47817-0ad1-408c-a6da-9a7b0fb2e34b">WsSetOutput</a> or <a href="https://msdn.microsoft.com/b969700d-7145-45eb-ad4b-c6e643975709">WsSetOutputToBuffer</a>functions to choose the encoding of the XML writer and to indicate where to direct the output.
      

A <a href="https://msdn.microsoft.com/8f413e60-8a30-492c-8f2d-80be511fee11">WS_XML_WRITER</a> can be reused by calling <a href="https://msdn.microsoft.com/f0b47817-0ad1-408c-a6da-9a7b0fb2e34b">WsSetOutput</a> or <a href="https://msdn.microsoft.com/b969700d-7145-45eb-ad4b-c6e643975709">WsSetOutputToBuffer</a> again.
      

See <a href="https://msdn.microsoft.com/c919eb01-bd15-4583-afcf-e46ac2fc9c8c">WS_XML_WRITER_PROPERTY_ID</a> for the properties that can be used to configure the writer.
      

The XML writer buffers all data until <a href="https://msdn.microsoft.com/ba631942-d5a0-4d93-9899-c3f0ebd4aae5">WsFlushWriter</a> is called.  This allows the caller to determine
        at what granularity to write data and to whether to write that data asynchronously.  Data is not written until
        <b>WsFlushWriter</b> is called.
      

If an operation on a  <a href="https://msdn.microsoft.com/8f413e60-8a30-492c-8f2d-80be511fee11">WS_XML_WRITER</a> fails the writer is left in a faulted state
        and further calls to the Writer return <b>WS_E_OBJECT_FAULTED</b>.  (See <a href="https://msdn.microsoft.com/96285557-8317-4875-b634-e2eacd605901">Windows Web Services Return Values</a>.)The only possible function calls for the XML writer
        if this occurs are <a href="https://msdn.microsoft.com/f0b47817-0ad1-408c-a6da-9a7b0fb2e34b">WsSetOutput</a> and <a href="https://msdn.microsoft.com/b969700d-7145-45eb-ad4b-c6e643975709">WsSetOutputToBuffer</a> to return the XML writer to a usable state,
        or <a href="https://msdn.microsoft.com/eb1eb835-838a-41e4-9e7d-c5c805237f65">WsFreeWriter</a> to free the XML writer.
      



