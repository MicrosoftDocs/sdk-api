---
UID: NF:webservices.WsEndWriterCanonicalization
title: WsEndWriterCanonicalization function (webservices.h)
description: This function stops XML canonicalization started by the preceding WsStartWriterCanonicalization call. Remaining canonical bytes buffered by the writer are written to the callback function.
helpviewer_keywords: ["WsEndWriterCanonicalization","WsEndWriterCanonicalization function [Web Services for Windows]","webservices/WsEndWriterCanonicalization","wsw.wsendwritercanonicalization"]
old-location: wsw\wsendwritercanonicalization.htm
tech.root: wsw
ms.assetid: 169f971e-0cd2-44e7-81fc-059cc3cd357d
ms.date: 12/05/2018
ms.keywords: WsEndWriterCanonicalization, WsEndWriterCanonicalization function [Web Services for Windows], webservices/WsEndWriterCanonicalization, wsw.wsendwritercanonicalization
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
 - WsEndWriterCanonicalization
 - webservices/WsEndWriterCanonicalization
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
 - WsEndWriterCanonicalization
---

# WsEndWriterCanonicalization function


## -description

This function stops XML canonicalization started by the preceding <a href="/windows/desktop/api/webservices/nf-webservices-wsstartwritercanonicalization">WsStartWriterCanonicalization</a> call.
      Remaining canonical bytes buffered by the writer are written to the callback function.

## -parameters

### -param writer [in]

A pointer to a  <a href="/windows/desktop/wsw/ws-xml-writer">WS_XML_WRITER</a> object on which canonicalization should be stopped.

### -param error [in, optional]

A  pointer to a <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> object where additional information about the error should be stored if the function fails.

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

<b>WsEndWriterCanonicalization</b> must be called at the same depth at
        which <a href="/windows/desktop/api/webservices/nf-webservices-wsstartwritercanonicalization">WsStartWriterCanonicalization</a> was called.
      

It is not necessary to call <b>WsEndWriterCanonicalization</b> in order to call <a href="/windows/desktop/api/webservices/nf-webservices-wsfreewriter">WsFreeWriter</a>.