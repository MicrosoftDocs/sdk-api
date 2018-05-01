---
UID: NF:certenroll.ICertProperty.InitializeDecode
title: ICertProperty::InitializeDecode method
author: windows-driver-content
description: Initializes the object from a byte array that contains the property value.
old-location: security\icertproperty_initializedecode_method.htm
old-project: SecCertEnroll
ms.assetid: 38b51242-cd4a-402e-b7ff-286f7bf66953
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: ICertProperty, ICertProperty interface [Security], InitializeDecode method, ICertProperty::InitializeDecode, InitializeDecode method [Security], InitializeDecode method [Security], ICertProperty interface, InitializeDecode,ICertProperty.InitializeDecode, certenroll/ICertProperty::InitializeDecode, security.icertproperty_initializedecode_method
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
-	ICertProperty.InitializeDecode
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ICertProperty::InitializeDecode method


## -description


The <b>InitializeDecode</b> method initializes the object from a byte array that contains the property value. The byte array is represented by a Unicode-encoded string.


## -parameters




### -param Encoding [in]

An <a href="https://msdn.microsoft.com/b42628ae-deed-497b-a20f-d175843b79c2">EncodingType</a> enumeration value that specifies the type of Unicode encoding applied to the input string.


### -param strEncodedData [in]

A <b>BSTR</b> variable that contains the <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) encoded property value.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table.  For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

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



Specify the property to initialize by calling the <a href="https://msdn.microsoft.com/2829dab5-253d-4ade-bba5-d399afe87a28">PropertyId</a> property. You can call the <a href="https://msdn.microsoft.com/1413f6da-0fcf-42ca-a79f-43f164368407">RawData</a> property to retrieve the encoded property value. Call the <a href="https://msdn.microsoft.com/46c409c4-46bd-4349-8363-1983f4411bc2">SetValueOnCertificate</a> method to associate the property value with a certificate.

If the <b>InitializeDecode</b> method fails, the <a href="https://msdn.microsoft.com/947c2f09-993d-4ced-8b76-66b79d96e3bc">ICertProperty</a> object is not initialized and the input property value is not saved. However, the <a href="https://msdn.microsoft.com/2829dab5-253d-4ade-bba5-d399afe87a28">PropertyId</a> property retains the specified identifier.

The <b>InitializeDecode</b> method is provided to enable you to initialize custom properties and properties identified in the <a href="https://msdn.microsoft.com/e7ad0ec5-a568-4506-ba54-908e00083c2b">CERTENROLL_PROPERTYID</a> enumeration for which there exist no specific interface. Each of the supported values in that enumeration contains information about the type of data, usually a <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_INTEGER_BLOB</a>, that you must supply to the <b>InitializeDecode</b> method. You can use the <a href="https://msdn.microsoft.com/495a321a-3005-4537-b082-5003e437d21f">IBinaryConverter</a> interface to convert a byte array to a string.

The following interfaces simplify creation of the most common properties:<ul>
<li>
<a href="https://msdn.microsoft.com/81219ad9-4717-40e5-9ecd-d3df980e23c6">ICertPropertyArchived</a>
</li>
<li>
<a href="https://msdn.microsoft.com/06696346-b9d1-4229-991e-539862cff3c9">ICertPropertyArchivedKeyHash</a>
</li>
<li>
<a href="https://msdn.microsoft.com/25eab0e9-4980-49ad-9d3b-35ad47c20bcb">ICertPropertyAutoEnroll</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9c694991-6f2d-420e-9f9f-5a36b10c39aa">ICertPropertyBackedUp</a>
</li>
<li>
<a href="https://msdn.microsoft.com/229e8ce9-fe18-45f4-8f91-cd741052a134">ICertPropertyDescription</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7530998b-b59c-426b-a74a-ead4bca55c3b">ICertPropertyEnrollment</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d2bfe2f2-423e-4620-8933-bbae4f98c62a">ICertPropertyFriendlyName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1c35c2f0-8e79-4031-bae2-2be081f3c8dd">ICertPropertyKeyProvInfo</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c87a391a-aec9-4b42-8084-c593ecbb0bc6">ICertPropertyRenewal</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ce33605e-c3ae-4b96-a13e-6f06e8d5ffee">ICertPropertyRequestOriginator</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0946827b-c933-472c-9466-aaa3495ab202">ICertPropertySHA1Hash</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/b830c0af-0a38-419d-8a33-8e3626c4e8f1">ICertProperties</a>



<a href="https://msdn.microsoft.com/947c2f09-993d-4ced-8b76-66b79d96e3bc">ICertProperty</a>
 

 

