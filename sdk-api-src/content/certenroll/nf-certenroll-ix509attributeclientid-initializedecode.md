---
UID: NF:certenroll.IX509AttributeClientId.InitializeDecode
title: IX509AttributeClientId::InitializeDecode
author: windows-sdk-content
description: Initializes the object from a Distinguished Encoding Rules (DER) encoded byte array that contains the attribute value.
old-location: security\ix509attributeclientid_initializedecode_method.htm
tech.root: SecCertEnroll
ms.assetid: 653b44fd-f69c-49e3-8aee-02445fa03cde
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IX509AttributeClientId interface [Security],InitializeDecode method, IX509AttributeClientId.InitializeDecode, IX509AttributeClientId::InitializeDecode, InitializeDecode, InitializeDecode method [Security], InitializeDecode method [Security],IX509AttributeClientId interface, certenroll/IX509AttributeClientId::InitializeDecode, security.ix509attributeclientid_initializedecode_method
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
 - IX509AttributeClientId.InitializeDecode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509AttributeClientId::InitializeDecode


## -description


The <b>InitializeDecode</b> method initializes the object from a  <a href="https://msdn.microsoft.com/en-us/library/ms721573(v=VS.85).aspx">Distinguished Encoding Rules</a> (DER) encoded byte array that contains the attribute value. The byte array is represented by a Unicode-encoded string.


## -parameters




### -param Encoding [in]

An <a href="https://msdn.microsoft.com/en-us/library/Aa374936(v=VS.85).aspx">EncodingType</a> enumeration value that specifies the type of Unicode encoding applied to the input string.


### -param strEncodedData [in]

A <b>BSTR</b> variable that contains the DER-encoded attribute.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -remarks



The <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifier</a> (OID) for this attribute is <b>XCN_OID_REQUEST_CLIENT_INFO</b> (1.3.6.1.4.1.311.21.20). For more information, see <a href="https://msdn.microsoft.com/en-us/library/Aa374855(v=VS.85).aspx">CERTENROLL_OBJECTID</a>.

You can use this method if you have a DER-encoded <a href="https://msdn.microsoft.com/en-us/library/ms721532(v=VS.85).aspx">Abstract Syntax Notation One</a> (ASN.1) object that contains the attribute value. You must supply the DER-encoded object in a Unicode encoded string. For more information, see the <a href="https://msdn.microsoft.com/en-us/library/Aa375047(v=VS.85).aspx">IBinaryConverter</a> interface.

You must call either <a href="https://msdn.microsoft.com/en-us/library/Aa377076(v=VS.85).aspx">InitializeEncode</a> or <b>InitializeDecode</b> before you can use an <a href="https://msdn.microsoft.com/en-us/library/Aa377073(v=VS.85).aspx">IX509AttributeClientId</a> object. The two methods complement each other. The <b>InitializeEncode</b> method enables you to construct an encoded ASN.1 structure from raw data, and the <b>InitializeDecode</b> method enables you to initialize raw data from an encoded ASN.1 structure. You can call the following properties to retrieve the raw data:<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377074(v=VS.85).aspx">ClientId</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377077(v=VS.85).aspx">MachineDnsName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377079(v=VS.85).aspx">ProcessName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377081(v=VS.85).aspx">UserSamName</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa377073(v=VS.85).aspx">IX509AttributeClientId</a>
 

 

