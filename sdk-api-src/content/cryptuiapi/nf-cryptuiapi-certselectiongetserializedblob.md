---
UID: NF:cryptuiapi.CertSelectionGetSerializedBlob
title: CertSelectionGetSerializedBlob function
author: windows-sdk-content
description: A helper function used to retrieve a serialized certificate BLOB from a CERT_SELECTUI_INPUT structure.
old-location: security\certselectiongetserializedblob.htm
old-project: SecCrypto
ms.assetid: 6c3240f7-5121-401d-a4d4-df3055cb301a
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: CertSelectionGetSerializedBlob, CertSelectionGetSerializedBlob function [Security], cryptuiapi/CertSelectionGetSerializedBlob, security.certselectiongetserializedblob
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: cryptuiapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: CTL_MODIFY_REQUEST, *PCTL_MODIFY_REQUEST
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Cryptui.dll
 - Ext-MS-Win-security-cryptui-l1-1-0.dll
 - ext-ms-win-security-cryptui-l1-1-1.dll
 - CertCredProviderOneCore.dll
api_name:
 - CertSelectionGetSerializedBlob
product: Windows
targetos: Windows
req.lib: 
req.dll: Cryptui.dll
req.irql: 
---

# CertSelectionGetSerializedBlob function


## -description


The <b>CertSelectionGetSerializedBlob</b> function is a helper function used to retrieve a serialized certificate <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a> from a <a href="https://msdn.microsoft.com/8953cddd-86b6-4781-8dca-b5fd3d298bc8">CERT_SELECTUI_INPUT</a> structure.


## -parameters




### -param pcsi [in]

A pointer to a <a href="https://msdn.microsoft.com/8953cddd-86b6-4781-8dca-b5fd3d298bc8">CERT_SELECTUI_INPUT</a> structure that contains the certificate store and certificate context chain information.


### -param ppOutBuffer [out]

The address of a pointer to a buffer that receives the serialized certificates BLOB.


### -param pulOutBufferSize [out]

A pointer to a <b>ULONG</b> to receive the size, in bytes, of the BLOB received in the buffer pointed to by the <i>ppOutBuffer</i> parameter.


## -returns



If the function succeeds, the function returns <b>S_OK</b>. 

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. 	If both <b>hStore</b> and <b>prgpChain</b> parameters are not <b>NULL</b>, return <b>E_INVALIDARG</b>. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.





## -remarks



The returned serialized BLOB is passed to the <a href="https://msdn.microsoft.com/946ac279-d30a-4a6c-a76d-d93597121427">CredUIPromptForWindowsCredentials</a> function in the <i>pvInAuthBuffer</i> parameter to allow a user to select a certificate by using the credential selection UI.

The certificates that are serialized in the BLOB returned in the buffer pointed to by the <i>ppOutBuffer</i>  parameter of this function are dependent on the values  of the <b>hStore</b> and <b>prgpChain</b> members of the <a href="https://msdn.microsoft.com/8953cddd-86b6-4781-8dca-b5fd3d298bc8">CERT_SELECTUI_INPUT</a> structure. 

<table>
<tr>
<th><b>hStore</b></th>
<th><b>prgpChain</b></th>
<th>Certificates serialized</th>
</tr>
<tr>
<td>
<b>NULL</b>

</td>
<td>
not <b>NULL</b>

</td>
<td>
The certificates pointed to by the <b>prgpChain</b> member are serialized.

</td>
</tr>
<tr>
<td>
not <b>NULL</b>

</td>
<td>
<b>NULL</b>

</td>
<td>
The certificates specified by the <b>hStore</b> member are serialized.

</td>
</tr>
<tr>
<td>
<b>NULL</b>

</td>
<td>
<b>NULL</b>

</td>
<td>
An empty BLOB is returned.

</td>
</tr>
<tr>
<td>
not <b>NULL</b>

</td>
<td>
not <b>NULL</b>

</td>
<td>
The call fails and the function returns <b>E_INVALIDARG</b>.

</td>
</tr>
</table>
 



