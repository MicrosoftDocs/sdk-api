---
UID: NF:webservices.WsRemoveNode
title: WsRemoveNode function
author: windows-sdk-content
description: Removes the node at the specified position from the xml buffer. If positioned on an element it will remove the element including all of its children and its corresponding end element, otherwise it will remove a single node.
old-location: wsw\wsremovenode.htm
tech.root: wsw
ms.assetid: 955fd0b3-b351-40db-a25f-dd1ed8b55550
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: WsRemoveNode, WsRemoveNode function [Web Services for Windows], webservices/WsRemoveNode, wsw.wsremovenode
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
 - WsRemoveNode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WsRemoveNode function


## -description


Removes the node at the specified position from the xml buffer.  If positioned 
        on an element it will remove the element including all of its children and its 
        corresponding end element, otherwise it will remove a single node.
      

The use of any API with a <a href="https://msdn.microsoft.com/7acbe407-e91b-435a-82bc-acbbc13cfcfd">WS_XML_READER</a> or <a href="https://msdn.microsoft.com/8f413e60-8a30-492c-8f2d-80be511fee11">WS_XML_WRITER</a> that 
        currently depends on this position or a child of this position will fail. The 
        WS_XML_READER or WS_XML_WRITER must be repositioned 
        before using further.
      

It will return <b>WS_E_INVALID_OPERATION</b> if the node is positioned on an end 
        element or the root of the document.
      (See <a href="https://msdn.microsoft.com/96285557-8317-4875-b634-e2eacd605901">Windows Web Services Return Values</a>.)

Calling <a href="https://msdn.microsoft.com/cc879cc0-c8ca-457e-9ff1-ae220e31cb04">WsSetReaderPosition</a> or <a href="https://msdn.microsoft.com/1d23bda1-d1da-44d4-9a9d-258bba200b29">WsSetWriterPosition</a> after calling <b>WsRemoveNode</b> will fail.
      


## -parameters




### -param nodePosition [in]

The position of the node that should be removed.
        


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
<dt><b>WS_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The operation is not allowed due to the current state of the object.

</td>
</tr>
</table>
 



