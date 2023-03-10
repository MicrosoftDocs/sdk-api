---
UID: NF:webservices.WsRemoveNode
title: WsRemoveNode function (webservices.h)
description: Removes the node at the specified position from the xml buffer. If positioned on an element it will remove the element including all of its children and its corresponding end element, otherwise it will remove a single node.
helpviewer_keywords: ["WsRemoveNode","WsRemoveNode function [Web Services for Windows]","webservices/WsRemoveNode","wsw.wsremovenode"]
old-location: wsw\wsremovenode.htm
tech.root: wsw
ms.assetid: 955fd0b3-b351-40db-a25f-dd1ed8b55550
ms.date: 12/05/2018
ms.keywords: WsRemoveNode, WsRemoveNode function [Web Services for Windows], webservices/WsRemoveNode, wsw.wsremovenode
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WsRemoveNode
 - webservices/WsRemoveNode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsRemoveNode
---

# WsRemoveNode function


## -description

Removes the node at the specified position from the xml buffer.  If positioned 
        on an element it will remove the element including all of its children and its 
        corresponding end element, otherwise it will remove a single node.
      

The use of any API with a <a href="/windows/desktop/wsw/ws-xml-reader">WS_XML_READER</a> or <a href="/windows/desktop/wsw/ws-xml-writer">WS_XML_WRITER</a> that 
        currently depends on this position or a child of this position will fail. The 
        WS_XML_READER or WS_XML_WRITER must be repositioned 
        before using further.
      

It will return <b>WS_E_INVALID_OPERATION</b> if the node is positioned on an end 
        element or the root of the document.
      (See <a href="/windows/desktop/wsw/windows-web-services-return-values">Windows Web Services Return Values</a>.)

Calling <a href="/windows/desktop/api/webservices/nf-webservices-wssetreaderposition">WsSetReaderPosition</a> or <a href="/windows/desktop/api/webservices/nf-webservices-wssetwriterposition">WsSetWriterPosition</a> after calling <b>WsRemoveNode</b> will fail.

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