---
UID: NF:certenroll.IX509CertificateRequestPkcs10.IsSmartCard
title: IX509CertificateRequestPkcs10::IsSmartCard
author: windows-sdk-content
description: Retrieves a Boolean value that indicates whether any of the cryptographic providers associated with the request object is a smart card provider.
old-location: security\ix509certificaterequestpkcs10_issmartcard_method.htm
tech.root: SecCertEnroll
ms.assetid: 663ca7dd-f108-46bf-9564-cd2d7ec2bb1f
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IX509CertificateRequestPkcs10 interface [Security],IsSmartCard method, IX509CertificateRequestPkcs10.IsSmartCard, IX509CertificateRequestPkcs10::IsSmartCard, IsSmartCard, IsSmartCard method [Security], IsSmartCard method [Security],IX509CertificateRequestPkcs10 interface, certenroll/IX509CertificateRequestPkcs10::IsSmartCard, security.ix509certificaterequestpkcs10_issmartcard_method
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
 - IX509CertificateRequestPkcs10.IsSmartCard
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509CertificateRequestPkcs10::IsSmartCard


## -description


The <b>IsSmartCard</b> method retrieves a Boolean value that indicates whether any of the cryptographic providers associated with the request object is a smart card provider.


## -parameters




### -param pValue [out]

Pointer to a <b>VARIANT_BOOL</b> variable that indicates whether any of the enumerated and selected providers is  a smart card provider.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.

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
The private key cannot be found, or the <a href="https://msdn.microsoft.com/en-us/library/Aa375967(v=VS.85).aspx">ICspInformation</a> object associated with the private key cannot be found.

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



The <b>IsSmartCard</b> method first checks the provider associated with the private key. If that provider is not for a smart card, the method iterates through the <a href="https://msdn.microsoft.com/en-us/library/Aa377517(v=VS.85).aspx">CspStatuses</a> collection until it finds a selected provider that is. If no selected smart card providers are found, the method returns <b>False</b>. You must initialize the <a href="https://msdn.microsoft.com/en-us/library/Aa377505(v=VS.85).aspx">IX509CertificateRequestPkcs10</a> object before calling this method. For more information, see any of the following methods:

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377520(v=VS.85).aspx">InitializeDecode</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377523(v=VS.85).aspx">InitializeFromCertificate</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377527(v=VS.85).aspx">InitializeFromPrivateKey</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377531(v=VS.85).aspx">InitializeFromPublicKey</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377533(v=VS.85).aspx">InitializeFromTemplateName</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa377505(v=VS.85).aspx">IX509CertificateRequestPkcs10</a>
 

 

