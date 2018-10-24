---
UID: NF:certenc.ICertEncodeCRLDistInfo.Encode
title: ICertEncodeCRLDistInfo::Encode
author: windows-sdk-content
description: Performs Abstract Syntax Notation One (ASN.1) encoding on a certificate revocation list (CRL) distribution information array stored in the COM object and returns the ASN.1-encoded extension.
old-location: security\icertencodecrldistinfo_encode.htm
tech.root: SecCrypto
ms.assetid: 46520e3a-1f15-4d1c-9f44-b9b420fb4f25
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: CCertEncodeCRLDistInfo object [Security],Encode method, Encode, Encode method [Security], Encode method [Security],CCertEncodeCRLDistInfo object, Encode method [Security],ICertEncodeCRLDistInfo interface, ICertEncodeCRLDistInfo interface [Security],Encode method, ICertEncodeCRLDistInfo.Encode, ICertEncodeCRLDistInfo::Encode, _certsrv_icertencodecrldistinfo_encode, certenc/ICertEncodeCRLDistInfo::Encode, security.icertencodecrldistinfo_encode
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Certidl.lib
req.dll: Certenc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenc.dll
api_name:
 - ICertEncodeCRLDistInfo.Encode
 - CCertEncodeCRLDistInfo.Encode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertEncodeCRLDistInfo::Encode


## -description


The <b>Encode</b> method performs <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) encoding on a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation list</a> (CRL) distribution information array stored in the COM object and returns the ASN.1-encoded extension.

 Before using this method, you must call the 
<a href="https://msdn.microsoft.com/899de888-918f-4202-a324-0e603eba2324">Reset</a> method to size the array and the 
<a href="https://msdn.microsoft.com/ce27adfd-e21a-4e8d-882e-72041f97958a">SetNameCount</a> and 
<a href="https://msdn.microsoft.com/fe33265a-8c75-4e16-8178-3569cf30d8e4">SetNameEntry</a> methods to set each element in each distribution point structure.


## -parameters




### -param pstrBinary

TBD




#### - pbstrBinary [out]

A pointer to a <b>BSTR</b> that will contain the encoded CRL distribution information extension. When you have finished using the <b>BSTR</b>, free it by calling the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the ASN.1-encoded string that represents the CRL distribution information array.




## -see-also




<a href="https://msdn.microsoft.com/e9c0053f-263f-4d7b-9356-bc33af989dbe">ICertEncodeCRLDistInfo</a>



<a href="https://msdn.microsoft.com/899de888-918f-4202-a324-0e603eba2324">ICertEncodeCRLDistInfo::Reset</a>



<a href="https://msdn.microsoft.com/ce27adfd-e21a-4e8d-882e-72041f97958a">ICertEncodeCRLDistInfo::SetNameCount</a>



<a href="https://msdn.microsoft.com/fe33265a-8c75-4e16-8178-3569cf30d8e4">ICertEncodeCRLDistInfo::SetNameEntry</a>
 

 

