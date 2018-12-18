---
UID: NF:webservices.WsSkipNode
title: WsSkipNode function
author: windows-sdk-content
description: Advances the reader in the input stream.
old-location: wsw\wsskipnode.htm
tech.root: wsw
ms.assetid: 90eda6f1-dda2-4595-90f5-029768278f5b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WsSkipNode, WsSkipNode function [Web Services for Windows], webservices/WsSkipNode, wsw.wsskipnode
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
 - WsSkipNode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WsSkipNode function


## -description


Advances the reader in the input stream.  If the current node is an element, 
        all of the children of that element are skipped, and the reader is positioned 
        on the node following its end element.  Otherwise, the reader is positioned 
        on the next node in the same manner as <a href="https://msdn.microsoft.com/60dacf3e-ebde-4247-be58-835565874ab6">WsReadNode</a>.
      


## -parameters




### -param reader [in]

The reader which is to skip to the next node.
        


### -param error [in, optional]

Specifies where additional error information should be stored if the function fails.
        


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
 




## -remarks



If there is an error parsing the input, the function will return <b>WS_E_INVALID_FORMAT</b>.
      (See <a href="https://msdn.microsoft.com/96285557-8317-4875-b634-e2eacd605901">Windows Web Services Return Values</a>.)

This function can fail for any of the reasons listed in <a href="https://msdn.microsoft.com/60dacf3e-ebde-4247-be58-835565874ab6">WsReadNode</a>.
      



