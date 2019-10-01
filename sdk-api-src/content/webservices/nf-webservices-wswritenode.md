---
UID: NF:webservices.WsWriteNode
title: WsWriteNode function (webservices.h)
author: windows-sdk-content
description: Writes the specified node to the XML Writer.
old-location: wsw\wswritenode.htm
tech.root: wsw
ms.assetid: ea2e511c-f3a6-415a-8a2d-a49e321b69d7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WsWriteNode, WsWriteNode function [Web Services for Windows], webservices/WsWriteNode, wsw.wswritenode
ms.topic: function
f1_keywords: 
 - "webservices/WsWriteNode"
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
 - WsWriteNode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WsWriteNode function


## -description


Writes the specified node to the XML Writer.
      


## -parameters




### -param writer [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/wsw/ws-xml-writer">WS_XML_WRITER</a> object to which the node is written.  The pointer must reference a valid <b>XML Writer</b> object.
                


### -param node [in]

A pointer to the Node object to write to the document.
        


### -param error [in, optional]

A  pointer to a <a href="https://docs.microsoft.com/windows/desktop/wsw/ws-error">WS_ERROR</a> object where additional information about the error should be stored if the function fails.
                


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
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_INVALID_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The input data was not in the expected format or did not have the expected value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_QUOTA_EXCEEDED</b></dt>
</dl>
</td>
<td width="60%">
A quota was exceeded.

</td>
</tr>
</table>
 



