---
UID: NF:certenroll.ICertProperty.InitializeDecode
title: ICertProperty::InitializeDecode
author: windows-sdk-content
description: Initializes the object from a byte array that contains the property value.
old-location: security\icertproperty_initializedecode_method.htm
tech.root: SecCertEnroll
ms.assetid: 38b51242-cd4a-402e-b7ff-286f7bf66953
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ICertProperty interface [Security],InitializeDecode method, ICertProperty.InitializeDecode, ICertProperty::InitializeDecode, InitializeDecode, InitializeDecode method [Security], InitializeDecode method [Security],ICertProperty interface, certenroll/ICertProperty::InitializeDecode, security.icertproperty_initializedecode_method
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
 - ICertProperty.InitializeDecode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertProperty::InitializeDecode


## -description


The <b>InitializeDecode</b> method initializes the object from a byte array that contains the property value. The byte array is represented by a Unicode-encoded string.


## -parameters




### -param Encoding [in]

An <a href="https://msdn.microsoft.com/en-us/library/Aa374936(v=VS.85).aspx">EncodingType</a> enumeration value that specifies the type of Unicode encoding applied to the input string.


### -param strEncodedData [in]

A <b>BSTR</b> variable that contains the <a href="https://msdn.microsoft.com/en-us/library/ms721573(v=VS.85).aspx">Distinguished Encoding Rules</a> (DER) encoded property value.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table.  For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.

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



Specify the property to initialize by calling the <a href="https://msdn.microsoft.com/en-us/library/Aa375830(v=VS.85).aspx">PropertyId</a> property. You can call the <a href="https://msdn.microsoft.com/en-us/library/Aa375836(v=VS.85).aspx">RawData</a> property to retrieve the encoded property value. Call the <a href="https://msdn.microsoft.com/en-us/library/Aa375928(v=VS.85).aspx">SetValueOnCertificate</a> method to associate the property value with a certificate.

If the <b>InitializeDecode</b> method fails, the <a href="https://msdn.microsoft.com/en-us/library/Aa375239(v=VS.85).aspx">ICertProperty</a> object is not initialized and the input property value is not saved. However, the <a href="https://msdn.microsoft.com/en-us/library/Aa375830(v=VS.85).aspx">PropertyId</a> property retains the specified identifier.

The <b>InitializeDecode</b> method is provided to enable you to initialize custom properties and properties identified in the <a href="https://msdn.microsoft.com/en-us/library/Aa374867(v=VS.85).aspx">CERTENROLL_PROPERTYID</a> enumeration for which there exist no specific interface. Each of the supported values in that enumeration contains information about the type of data, usually a <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_INTEGER_BLOB</a>, that you must supply to the <b>InitializeDecode</b> method. You can use the <a href="https://msdn.microsoft.com/en-us/library/Aa375047(v=VS.85).aspx">IBinaryConverter</a> interface to convert a byte array to a string.

The following interfaces simplify creation of the most common properties:<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa375240(v=VS.85).aspx">ICertPropertyArchived</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa375241(v=VS.85).aspx">ICertPropertyArchivedKeyHash</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa375250(v=VS.85).aspx">ICertPropertyAutoEnroll</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa375353(v=VS.85).aspx">ICertPropertyBackedUp</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa375646(v=VS.85).aspx">ICertPropertyDescription</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa375665(v=VS.85).aspx">ICertPropertyEnrollment</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa375715(v=VS.85).aspx">ICertPropertyFriendlyName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa375725(v=VS.85).aspx">ICertPropertyKeyProvInfo</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa375749(v=VS.85).aspx">ICertPropertyRenewal</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa375772(v=VS.85).aspx">ICertPropertyRequestOriginator</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa375792(v=VS.85).aspx">ICertPropertySHA1Hash</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa375231(v=VS.85).aspx">ICertProperties</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375239(v=VS.85).aspx">ICertProperty</a>
 

 

