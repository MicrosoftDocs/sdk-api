---
UID: NF:webservices.WsReadNode
title: WsReadNode function
author: windows-sdk-content
description: This operation advances the Reader to the next node in the input stream.
old-location: wsw\wsreadnode.htm
tech.root: wsw
ms.assetid: 60dacf3e-ebde-4247-be58-835565874ab6
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WsReadNode, WsReadNode function [Web Services for Windows], webservices/WsReadNode, wsw.wsreadnode
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
 - WsReadNode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WsReadNode function


## -description


This operation advances the Reader to the next <a href="https://msdn.microsoft.com/98c40d57-ee71-40f8-9416-5b29adc30489">node</a> in the input stream.
      If there is an error parsing the input the function will return <b>WS_E_INVALID_FORMAT</b>.
      (See <a href="https://msdn.microsoft.com/96285557-8317-4875-b634-e2eacd605901">Windows Web Services Return Values</a>.)


## -parameters




### -param reader [in]

A pointer to the <b>XML Reader</b> object to advance.
          The pointer must reference a valid <a href="https://msdn.microsoft.com/7acbe407-e91b-435a-82bc-acbbc13cfcfd">WS_XML_READER</a> and it may not be <b>NULL</b>.
                


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
<dt><b>WS_E_INVALID_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The input data was not in the expected format, or did not have the expected value, or multiple top-level elements were found and <b>WS_XML_READER_PROPERTY_ALLOW_FRAGMENT</b> is <b>FALSE</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_QUOTA_EXCEEDED</b></dt>
</dl>
</td>
<td width="60%">
An element was read that exceeded some limit such as <b>WS_XML_READER_PROPERTY_MAX_DEPTH</b> or <b>WS_XML_READER_PROPERTY_MAX_ATTRIBUTES</b>.

</td>
</tr>
</table>
 




## -remarks



Other exception conditions include: <ul>
<li>If an XML declaration is found and <b>WS_XML_READER_PROPERTY_READ_DECLARATION</b> is <b>FALSE</b>,
        <b>WS_E_INVALID_FORMAT</b> is returned.
      </li>
<li>If the Reader is using <a href="https://msdn.microsoft.com/53537eb2-6b8d-443e-9453-4b39dfef1dd7">WS_XML_READER_STREAM_INPUT</a> and there was insufficient data buffered the reader will return
        <b>WS_E_QUOTA_EXCEEDED</b>.
      </li>
</ul>




