---
UID: NF:certenroll.IX509CertificateRequest.GetInnerRequest
title: IX509CertificateRequest::GetInnerRequest
author: windows-sdk-content
description: Retrieves a nested request object.
old-location: security\ix509certificaterequest_getinnerrequest_method.htm
tech.root: seccertenroll
ms.assetid: 5ade7824-d95a-492d-aadf-487422386500
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetInnerRequest, GetInnerRequest method [Security], GetInnerRequest method [Security],IX509CertificateRequest interface, IX509CertificateRequest interface [Security],GetInnerRequest method, IX509CertificateRequest.GetInnerRequest, IX509CertificateRequest::GetInnerRequest, certenroll/IX509CertificateRequest::GetInnerRequest, security.ix509certificaterequest_getinnerrequest_method
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
 - IX509CertificateRequest.GetInnerRequest
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509CertificateRequest::GetInnerRequest


## -description


The <b>GetInnerRequest</b> method retrieves a nested request object.


## -parameters




### -param Level [in]

 A value of an <a href="https://msdn.microsoft.com/57b16024-5347-4218-90a7-d85e403aacf0">InnerRequestLevel</a> enumeration that specifies the envelopment level of the data to retrieve. You can use the <i>LevelNext</i> value to iterate through the nested levels or the <i>LevelInnermost</i> value to retrieve the most deeply nested request object. You cannot specify <i>LevelNext</i> for a PKCS #10 request.


### -param ppValue [out]

Address of a variable that receives a pointer to an <a href="https://msdn.microsoft.com/5425c9ab-565d-449d-87e1-e5765868acfb">IX509CertificateRequest</a> interface that contains the nested request. Call the <a href="https://msdn.microsoft.com/04e7e4eb-8f65-45d3-bf1d-abcb83fcf1a0">Type</a> property to determine whether the inner request object is a PKCS #10 or a CMC request. Then call <b>QueryInterface</b> to retrieve the appropriate pointer.


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
You specified a value of <i>LevelNext</i> PKCS #10 request.

</td>
</tr>
</table>
 




## -remarks



A top-level request object can be a PKCS #10, PKCS #7, or CMC request. The following rules apply to inner request objects:<ul>
<li>A PKCS #10 request cannot contain an inner request object.</li>
<li>A PKCS #7 request can contain only a PKCS #10 inner request object.</li>
<li>A CMC request can contain a CMC or a PKCS #10 inner request object. For a CMC request that contains an inner CMC request, there is no theoretical limit to the number of nested levels that can exist before the final inner PKCS #10 request is reached. That is, a top-level CMC request can contain an inner CMC request that also contains an inner CMC request and so on.</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/5425c9ab-565d-449d-87e1-e5765868acfb">IX509CertificateRequest</a>



<a href="https://msdn.microsoft.com/7197a225-b2dc-47bb-8843-d3fb4bf95811">IX509CertificateRequestCertificate</a>



<a href="https://msdn.microsoft.com/77059388-c442-4db5-ab27-1db25e2f63b9">IX509CertificateRequestCmc</a>



<a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a>



<a href="https://msdn.microsoft.com/ae869557-6523-4387-835e-c9631898d864">IX509CertificateRequestPkcs7</a>



<a href="https://msdn.microsoft.com/25774ccb-8e76-443d-89da-177d6e77c019">IX509SignatureInformation</a>
 

 

