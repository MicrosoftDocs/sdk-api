---
UID: NF:certenc.ICertEncodeDateArray.Encode
title: ICertEncodeDateArray::Encode
author: windows-sdk-content
description: Returns an Abstract Syntax Notation One (ASN.1)-encoded string of the date array stored in this object.
old-location: security\icertencodedatearray_encode.htm
old-project: SecCrypto
ms.assetid: 102ca165-c320-4e18-986f-7375fbc617e0
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: CCertEncodeDateArray object [Security],Encode method, Encode, Encode method [Security], Encode method [Security],CCertEncodeDateArray object, Encode method [Security],ICertEncodeDateArray interface, ICertEncodeDateArray interface [Security],Encode method, ICertEncodeDateArray.Encode, ICertEncodeDateArray::Encode, _certsrv_icertencodedatearray_encode, certenc/ICertEncodeDateArray::Encode, security.icertencodedatearray_encode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: certenc.h
req.include-header: Certsrv.h
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
tech.root: 
req.typenames: X509EnrollmentAuthFlags
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenc.dll
api_name:
 - ICertEncodeDateArray.Encode
 - CCertEncodeDateArray.Encode
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certenc.dll
req.irql: 
---

# ICertEncodeDateArray::Encode


## -description


The <b>Encode</b> method returns an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1)-encoded string of the date array stored in this object.

Use the <a href="https://msdn.microsoft.com/79937ef7-4b1a-4132-9ef4-23b2857c7fac">Decode</a> method to decode the encoded string into an <b>CertEncodeDateArray</b> object.

Before using this method, you must call both the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a> method to size the array and the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597642">SetValue</a> method to set each array element.


## -parameters




### -param pstrBinary






#### - pbstrBinary [out]

A pointer to a <b>BSTR</b> that will contain the encoded <b>Date</b> array. When you have finished using the <b>BSTR</b>, free it by calling the <a href="https://msdn.microsoft.com/library/ms221481(v=VS.85).aspx">SysFreeString</a> function.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the ASN.1-encoded string that represents the <b>DATE</b> array.




## -see-also




<a href="https://msdn.microsoft.com/9973c49a-d886-4cc4-b75e-7ff46f56d51c">ICertEncodeDateArray</a>



<a href="https://msdn.microsoft.com/79937ef7-4b1a-4132-9ef4-23b2857c7fac">ICertEncodeDateArray::Decode</a>



<a href="https://msdn.microsoft.com/f09087aa-ae10-4a59-9b59-5f8b72254ce6">ICertEncodeDateArray::Reset</a>



<a href="https://msdn.microsoft.com/e05a7aa1-81ad-4564-a6a5-65b8ac816598">ICertEncodeDateArray::SetValue</a>
 

 

