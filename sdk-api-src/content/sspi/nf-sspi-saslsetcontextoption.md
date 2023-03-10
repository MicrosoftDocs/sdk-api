---
UID: NF:sspi.SaslSetContextOption
title: SaslSetContextOption function (sspi.h)
description: Sets the value of the specified property for the specified SASL context.
helpviewer_keywords: ["SASL_OPTION_AUTHZ_PROCESSING","SASL_OPTION_AUTHZ_STRING","SASL_OPTION_RECV_SIZE","SASL_OPTION_SEND_SIZE","SaslSetContextOption","SaslSetContextOption function [Security]","security.saslsetcontextoption","sspi/SaslSetContextOption"]
old-location: security\saslsetcontextoption.htm
tech.root: security
ms.assetid: 3c3b1209-b0de-4100-8dfe-53ea314b790b
ms.date: 12/05/2018
ms.keywords: SASL_OPTION_AUTHZ_PROCESSING, SASL_OPTION_AUTHZ_STRING, SASL_OPTION_RECV_SIZE, SASL_OPTION_SEND_SIZE, SaslSetContextOption, SaslSetContextOption function [Security], security.saslsetcontextoption, sspi/SaslSetContextOption
req.header: sspi.h
req.include-header: Security.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Secur32.lib
req.dll: Secur32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SaslSetContextOption
 - sspi/SaslSetContextOption
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Secur32.dll
api_name:
 - SaslSetContextOption
---

# SaslSetContextOption function


## -description

The <b>SaslSetContextOption</b> function sets the value of the specified property for the specified SASL context.

## -parameters

### -param ContextHandle [in]

Handle of the SASL context.

### -param Option [in]

Property to set for the SASL context. The following table lists the possible values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SASL_OPTION_AUTHZ_PROCESSING"></a><a id="sasl_option_authz_processing"></a><dl>
<dt><b>SASL_OPTION_AUTHZ_PROCESSING</b></dt>
</dl>
</td>
<td width="60%">
Data type of buffer: <b>ULONG</b>

State of SASL processing of the Authz value provided by the SASL application. The valid states for processing are Sasl_AuthZIDForbidden  and Sasl_AuthZIDProcessed. The default value is Sasl_AuthZIDProcessed.

</td>
</tr>
<tr>
<td width="40%"><a id="SASL_OPTION_AUTHZ_STRING"></a><a id="sasl_option_authz_string"></a><dl>
<dt><b>SASL_OPTION_AUTHZ_STRING</b></dt>
</dl>
</td>
<td width="60%">
Data type of buffer: Array of binary characters

String of characters passed from the SASL client to the server.  If the AuthZ_Processing state is Sasl_AuthZIDForbidden, the  return value SEC_E_UNSUPPORTED_FUNCTION is returned.

</td>
</tr>
<tr>
<td width="40%"><a id="SASL_OPTION_RECV_SIZE"></a><a id="sasl_option_recv_size"></a><dl>
<dt><b>SASL_OPTION_RECV_SIZE</b></dt>
</dl>
</td>
<td width="60%">
Data type of buffer: <b>ULONG</b>

Maximum size of the receiving buffer on the local computer. The default value is 0x0FFFF bytes.

</td>
</tr>
<tr>
<td width="40%"><a id="SASL_OPTION_SEND_SIZE"></a><a id="sasl_option_send_size"></a><dl>
<dt><b>SASL_OPTION_SEND_SIZE</b></dt>
</dl>
</td>
<td width="60%">
Data type of buffer: <b>ULONG</b>

Maximum message data size that can be transmitted.  This value is  the maximum buffer size that can be transmitted to the remote SASL process minus the block size, the trailer size, and the maximum signature size. The default value is 0x0FFFF bytes.

</td>
</tr>
</table>

### -param Value [in]

A pointer to a buffer that contains the value to set to  the requested property. For the data type of the buffer for each value of the <i>Option</i> parameter, see the <i>Option</i> parameter.

### -param Size [in]

The size, in bytes, of the buffer specified by the <i>Value</i> parameter.

## -returns

If the call is completed successfully, this function returns SEC_E_OK. The following table shows some possible error return values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_BUFFER_TOO_SMALL</b></dt>
</dl>
</td>
<td width="60%">
The buffer specified by the <i>Value</i> parameter is not large enough to contain the data value of the property specified by the <i>Option</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The SASL context handle specified by the <i>ContextHandle</i> parameter was not found in the SASL list.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_UNSUPPORTED_FUNCTION</b></dt>
</dl>
</td>
<td width="60%">
The option specified in the <i>Option</i> parameter is not valid.

</td>
</tr>
</table>

