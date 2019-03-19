---
UID: NF:webservices.WsSetOutputToBuffer
title: WsSetOutputToBuffer function (webservices.h)
author: windows-sdk-content
description: This operation positions the Writer at the end of the specified buffer.
old-location: wsw\wssetoutputtobuffer.htm
tech.root: wsw
ms.assetid: b969700d-7145-45eb-ad4b-c6e643975709
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WsSetOutputToBuffer, WsSetOutputToBuffer function [Web Services for Windows], webservices/WsSetOutputToBuffer, wsw.wssetoutputtobuffer
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
 - WsSetOutputToBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WsSetOutputToBuffer function


## -description


This operation positions the Writer at the end of the specified buffer.
      
        When an XML Writer has an XML Buffer set as output the Writer can be used in a "random access" fashion and
        the functions <a href="https://msdn.microsoft.com/0c0fbd78-ed4f-40da-a63d-a2f38136ecb3">WsGetWriterPosition</a>, <a href="https://msdn.microsoft.com/1d23bda1-d1da-44d4-9a9d-258bba200b29">WsSetWriterPosition</a> and <a href="https://msdn.microsoft.com/f8eace53-9fa5-466a-8894-3c8b8fe049e3">WsMoveWriter</a> can be used.
      Properties
        specified for this function override those specified with the <code>WsCreateWriter</code> function. <div class="alert"><b>Note</b>  See <a href="https://msdn.microsoft.com/5b4bb009-764e-4892-903a-5939f5570016">WsCreateWriter</a> for the default values of the properties of the writer.
      </div>
<div> </div>



## -parameters




### -param writer [in]

A pointer to the <a href="https://msdn.microsoft.com/8f413e60-8a30-492c-8f2d-80be511fee11">WS_XML_WRITER</a> object for which the output is set.  The pointer must reference a valid <b>XML Writer</b> object.
                


### -param buffer [in]

A pointer to the buffer where the Writer sends the data.
        


### -param properties

A WS_XML_WRITER_PROPERTY pointer that  references an "array" of optional Writer properties.  


### -param propertyCount [in]

The number of properties.


### -param error [in, optional]

A  pointer to a <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> object where additional information about the error should be stored if the function fails.
                


## -returns



This function can return one of these values.

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



See <a href="https://msdn.microsoft.com/5b4bb009-764e-4892-903a-5939f5570016">WsCreateWriter</a> for the default values of the properties of the writer.
      



