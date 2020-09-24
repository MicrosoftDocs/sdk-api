---
UID: NF:wsman.WSManGetErrorMessage
title: WSManGetErrorMessage function (wsman.h)
description: Retrieves the error messages associated with a particular error and language codes.
helpviewer_keywords: ["WSManGetErrorMessage","WSManGetErrorMessage function [Windows Remote Management]","winrm.wsmangeterrormessage","wsman/WSManGetErrorMessage"]
old-location: winrm\wsmangeterrormessage.htm
tech.root: winrm
ms.assetid: 95fbded5-859d-4111-914c-871a05530726
ms.date: 12/05/2018
ms.keywords: WSManGetErrorMessage, WSManGetErrorMessage function [Windows Remote Management], winrm.wsmangeterrormessage, wsman/WSManGetErrorMessage
req.header: wsman.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WsmSvc.lib
req.dll: WsmSvc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework on Windows Server 2008 with SP2 and Windows Vista with SP2
ms.custom: 19H1
f1_keywords:
 - WSManGetErrorMessage
 - wsman/WSManGetErrorMessage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WsmSvc.dll
api_name:
 - WSManGetErrorMessage
---

# WSManGetErrorMessage function


## -description

Retrieves the error messages associated with a particular error and language codes.

## -parameters

### -param apiHandle [in]

Specifies the API handle returned by a <a href="/windows/desktop/api/wsman/nf-wsman-wsmaninitialize">WSManInitialize</a> call. This parameter  cannot be <b>NULL</b>.

### -param flags

Reserved for future use. Must be zero.

### -param languageCode [in, optional]

Specifies the language code name that should be used to localize the error. For more information about the language code names, see the    RFC 3066 specification from the Internet Engineering Task Force at <a href="https://www.ietf.org/rfc/rfc3066.txt">http://www.ietf.org/rfc/rfc3066.txt</a>.  If a language code is not specified, the user interface language of the thread is  used.

### -param errorCode

Specifies the error code for the requested error message. This error code can be a hexadecimal or decimal error code from a WinRM, WinHTTP, or other Windows operating system feature.

### -param messageLength

Specifies the number of characters that can be stored in the output message buffer, including the <b>null</b> terminator. If this parameter is zero, the <i>message</i> parameter must be <b>NULL</b>.

### -param message [out]

Specifies the output buffer to store the message in. This buffer must be allocated and deallocated by the client. The buffer must be large enough to store the message and the <b>null</b> terminator. If this parameter is <b>NULL</b>, the <i>messageLength</i> parameter must be <b>NULL</b>.

### -param messageLengthUsed [out]

Specifies the actual number of characters written to the output buffer, including the <b>null</b> terminator. This parameter cannot be <b>NULL</b>. If either the <i>messageLength</i> or <i>message</i> parameters are zero, the function will return <b>ERROR_INSUFFICIENT_BUFFER</b> and this parameter will be set to the number of characters needed to store the message, including the <b>null</b> terminator.

## -returns

This method returns zero on success. Otherwise, this method returns an error code.