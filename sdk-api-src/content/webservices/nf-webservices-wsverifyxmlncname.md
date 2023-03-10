---
UID: NF:webservices.WsVerifyXmlNCName
title: WsVerifyXmlNCName function (webservices.h)
description: Verifies whether the input string is a valid XML NCName.
helpviewer_keywords: ["WsVerifyXmlNCName","WsVerifyXmlNCName function [Web Services for Windows]","webservices/WsVerifyXmlNCName","wsw.wsverifyxmlncname"]
old-location: wsw\wsverifyxmlncname.htm
tech.root: wsw
ms.assetid: af9953c0-481d-4aa8-b938-e10d5d733a59
ms.date: 12/05/2018
ms.keywords: WsVerifyXmlNCName, WsVerifyXmlNCName function [Web Services for Windows], webservices/WsVerifyXmlNCName, wsw.wsverifyxmlncname
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
 - WsVerifyXmlNCName
 - webservices/WsVerifyXmlNCName
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
 - WsVerifyXmlNCName
---

# WsVerifyXmlNCName function


## -description

Verifies whether the input string is a valid XML NCName.

## -parameters

### -param ncNameChars

The string to be verified.

### -param ncNameCharCount [in]

The length of the <i>ncNameChars</i> string.

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
The string is not a valid NCName.

</td>
</tr>
</table>

