---
UID: NF:certenroll.IX509CertificateRequest.ResetForEncode
title: IX509CertificateRequest::ResetForEncode
author: windows-sdk-content
description: Restores the state of the request object to that which existed before the Encode method was called.
old-location: security\ix509certificaterequest_resetforencode_method.htm
tech.root: SecCertEnroll
ms.assetid: 7f0bd391-c456-467a-8bc1-6f0a8bd21e24
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IX509CertificateRequest interface [Security],ResetForEncode method, IX509CertificateRequest.ResetForEncode, IX509CertificateRequest::ResetForEncode, ResetForEncode, ResetForEncode method [Security], ResetForEncode method [Security],IX509CertificateRequest interface, certenroll/IX509CertificateRequest::ResetForEncode, security.ix509certificaterequest_resetforencode_method
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509CertificateRequest.ResetForEncode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- certenroll.h
: 
- IX509CertificateRequest.ResetForEncode
: 
---

# IX509CertificateRequest::ResetForEncode


## -description


The <b>ResetForEncode</b> method restores the state of the request object to that which existed before the <a href="https://msdn.microsoft.com/098788f4-539f-420b-a4e1-65625dd56ca1">Encode</a> method was called.


## -parameters






## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>CERTSRV_E_PROPERTY_EMPTY</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Certificate extensions and attributes have not been defined.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>HRESULT_FROM_WIN32(ERROR_INVALID_STATE)</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The request object is not encoded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>OLE_E_BLANK</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The object is not initialized.

</td>
</tr>
</table>
 




## -remarks



You can use this method to reconfigure (re-encode and re-sign) a certificate request in response to rejection of the request by a certification authority.  The signature and the raw data are cleared. The extensions and attributes are reset to the values they had before the <a href="https://msdn.microsoft.com/098788f4-539f-420b-a4e1-65625dd56ca1">Encode</a> method was called, but critical extension flags are not. For a CMC request object, each nested request is also reset.

This method is typically used for a CMC key archival request when the private key is encrypted and included in the request.




## -see-also




<a href="https://msdn.microsoft.com/5425c9ab-565d-449d-87e1-e5765868acfb">IX509CertificateRequest</a>



<a href="https://msdn.microsoft.com/7197a225-b2dc-47bb-8843-d3fb4bf95811">IX509CertificateRequestCertificate</a>



<a href="https://msdn.microsoft.com/77059388-c442-4db5-ab27-1db25e2f63b9">IX509CertificateRequestCmc</a>



<a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a>



<a href="https://msdn.microsoft.com/ae869557-6523-4387-835e-c9631898d864">IX509CertificateRequestPkcs7</a>



<a href="https://msdn.microsoft.com/25774ccb-8e76-443d-89da-177d6e77c019">IX509SignatureInformation</a>
 

 

