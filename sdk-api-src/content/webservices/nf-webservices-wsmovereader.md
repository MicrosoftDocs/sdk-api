---
UID: NF:webservices.WsMoveReader
title: WsMoveReader function (webservices.h)
description: Moves the current position of the reader as specified by the moveTo parameter. This function can only be used on a reader that is set to an XmlBuffer.
helpviewer_keywords: ["WsMoveReader","WsMoveReader function [Web Services for Windows]","webservices/WsMoveReader","wsw.wsmovereader"]
old-location: wsw\wsmovereader.htm
tech.root: wsw
ms.assetid: 63d18407-f82b-4884-a162-2c8163e883e1
ms.date: 12/05/2018
ms.keywords: WsMoveReader, WsMoveReader function [Web Services for Windows], webservices/WsMoveReader, wsw.wsmovereader
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
 - WsMoveReader
 - webservices/WsMoveReader
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
 - WsMoveReader
---

# WsMoveReader function


## -description

Moves the current position of the reader as specified by the <i>moveTo</i> parameter.
      
This function can only be used on a reader that is set to an XmlBuffer.

## -parameters

### -param reader [in]

A pointer to the <b>XML Reader</b> object with the position to move.  The pointer must reference a valid <a href="/windows/desktop/wsw/ws-xml-reader">WS_XML_READER</a> object and the referenced <b>Reader</b> value may not be <b>NULL</b>.

### -param moveTo [in]

This enumerator specifies direction or next position of the Reader relative to the current position.

### -param found

Indicates success or failure of the specified move.

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
<dt><b>WS_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The operation is not allowed due to the current state of the object.

</td>
</tr>
</table>

## -remarks

If the found parameter is not <b>NULL</b>, then it will indicate there whether or not it could
        move to the requested node and return NOERROR.
      

If the found parameter is <b>NULL</b>, and the requested node is not found, it will return <b>WS_E_INVALID_FORMAT</b>.
      (See <a href="/windows/desktop/wsw/windows-web-services-return-values">Windows Web Services Return Values</a>.) 

This function cannot be used while canonicalizing.  If <a href="/windows/desktop/api/webservices/nf-webservices-wsstartreadercanonicalization">WsStartReaderCanonicalization</a> has
        been called, then it will return <b>WS_E_INVALID_OPERATION</b>.