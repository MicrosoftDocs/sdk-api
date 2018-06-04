---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# WsWriteText function


## -description


Writes the specified text to the XML writer.
      
        To write characters to an attribute value call <a href="https://msdn.microsoft.com/9fd1eed9-6d8b-4b2e-a7ad-54a7f584734f">WsWriteStartAttribute</a>. Only whitespace characters may be written at the root of an xml document unless the
        <b>WS_XML_WRITER_PROPERTY_ALLOW_FRAGMENT</b> has been set to <b>TRUE</b>.
      






## -parameters




### -param writer [in]

A pointer to the <a href="https://msdn.microsoft.com/8f413e60-8a30-492c-8f2d-80be511fee11">WS_XML_WRITER</a> object to which the text is written.  The pointer must reference a valid <b>XML Writer</b> object.
                


### -param text [in]

A pointer to the text to write.  <div class="alert"><b>Note</b>  See <a href="https://msdn.microsoft.com/430edd13-b664-4e10-8d61-ffa6a01dcb90">WS_XML_TEXT</a> and its derived classes for more information on the text object.
        </div>
<div> </div>



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
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">

The operation is not allowed due to the current state of the object.

</td>
</tr>
</table>
 




## -remarks



<b>WsWriteText</b> can be called only once between <a href="https://msdn.microsoft.com/9fd1eed9-6d8b-4b2e-a7ad-54a7f584734f">WsWriteStartAttribute</a> and <a href="https://msdn.microsoft.com/8747c484-19b3-46b2-beee-80b220011def">WsWriteEndAttribute</a> 
        unless the text type is one of the following:
        <ul>
<li><b>WS_XML_TEXT_TYPE_UTF8</b></li>
<li><b>WS_XML_TEXT_TYPE_UTF16</b></li>
<li><b>WS_XML_TEXT_TYPE_BASE64</b></li>
</ul>
<div class="alert"><b>Note</b>  If the text Type is set to either of the previous values WsWriteText can be called more than once.  However the text Type must be the same for all calls within an attribute.
      </div>
<div> </div>




