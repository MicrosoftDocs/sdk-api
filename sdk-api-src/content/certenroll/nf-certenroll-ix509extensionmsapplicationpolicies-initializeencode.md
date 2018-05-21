---
UID: NF:certenroll.IX509ExtensionMSApplicationPolicies.InitializeEncode
title: IX509ExtensionMSApplicationPolicies::InitializeEncode
author: windows-driver-content
description: Initializes the extension from an ICertificatePolicies collection.
old-location: security\ix509extensionmsapplicationpolicies_initializeencode_method.htm
old-project: SecCertEnroll
ms.assetid: 2b79c295-5260-4708-9a20-2ac41052a171
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: IX509ExtensionMSApplicationPolicies interface [Security],InitializeEncode method, IX509ExtensionMSApplicationPolicies.InitializeEncode, IX509ExtensionMSApplicationPolicies::InitializeEncode, InitializeEncode, InitializeEncode method [Security], InitializeEncode method [Security],IX509ExtensionMSApplicationPolicies interface, certenroll/IX509ExtensionMSApplicationPolicies::InitializeEncode, security.ix509extensionmsapplicationpolicies_initializeencode_method
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
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CertEnroll.dll
api_name:
-	IX509ExtensionMSApplicationPolicies.InitializeEncode
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509ExtensionMSApplicationPolicies::InitializeEncode


## -description


The <b>InitializeEncode</b> method initializes the extension from an <a href="https://msdn.microsoft.com/2503adcb-0b73-42ef-98cf-a2b906e34ef7">ICertificatePolicies</a> collection.


## -parameters




### -param pValue [in]

Pointer to the <a href="https://msdn.microsoft.com/2503adcb-0b73-42ef-98cf-a2b906e34ef7">ICertificatePolicies</a> interface.


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
<dt><b><b>HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The object is already initialized.

</td>
</tr>
</table>
 




## -remarks



You must call either <b>InitializeEncode</b> or <a href="https://msdn.microsoft.com/b99d756c-01fd-4bde-a64b-c908626e9190">InitializeDecode</a> before you can use an  <a href="https://msdn.microsoft.com/35b6449e-5a82-4f47-bdda-5356f44bb1fd">IX509ExtensionMSApplicationPolicies</a> object. The two methods complement each other. The <b>InitializeEncode</b> method enables you to construct a <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) encoded ASN.1 extension object from raw data, and the <b>InitializeDecode</b> method enables you to initialize the raw data from an encoded object.

You can retrieve the following properties for this extension:<ul>
<li>The <a href="https://msdn.microsoft.com/library/windows/hardware/mt158256">Critical</a> property identifies whether the extension is critical. You can also specify this property.</li>
<li>The <a href="https://msdn.microsoft.com/d3508bfe-e323-4075-9c82-d9b53b8f54aa">ObjectId</a> property retrieves the extension <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID).</li>
<li>The <a href="https://msdn.microsoft.com/library/windows/hardware/dn965797">Policies</a> property retrieves the collection of <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate policies</a> (the raw extension data).</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/35b6449e-5a82-4f47-bdda-5356f44bb1fd">IX509ExtensionMSApplicationPolicies</a>



<a href="https://msdn.microsoft.com/b99d756c-01fd-4bde-a64b-c908626e9190">InitializeDecode</a>
 

 

