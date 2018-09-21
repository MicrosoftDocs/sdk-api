---
UID: NF:certenc.ICertEncodeCRLDistInfo.Encode
title: ICertEncodeCRLDistInfo::Encode
author: windows-sdk-content
description: Performs Abstract Syntax Notation One (ASN.1) encoding on a certificate revocation list (CRL) distribution information array stored in the COM object and returns the ASN.1-encoded extension.
old-location: security\icertencodecrldistinfo_encode.htm
tech.root: seccrypto
ms.assetid: 46520e3a-1f15-4d1c-9f44-b9b420fb4f25
ms.author: windowssdkdev
ms.date: 09/19/2018
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


The <b>Encode</b> method performs <a href="https://msdn.microsoft.com/en-us/library/ms721532(v=VS.85).aspx">Abstract Syntax Notation One</a> (ASN.1) encoding on a <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certificate revocation list</a> (CRL) distribution information array stored in the COM object and returns the ASN.1-encoded extension.

 Before using this method, you must call the 
<a href="https://msdn.microsoft.com/en-us/library/Aa383969(v=VS.85).aspx">Reset</a> method to size the array and the 
<a href="https://msdn.microsoft.com/en-us/library/Aa383982(v=VS.85).aspx">SetNameCount</a> and 
<a href="https://msdn.microsoft.com/en-us/library/Aa383985(v=VS.85).aspx">SetNameEntry</a> methods to set each element in each distribution point structure.


## -parameters




### -param pstrBinary

TBD




#### - pbstrBinary [out]

A pointer to a <b>BSTR</b> that will contain the encoded CRL distribution information extension. When you have finished using the <b>BSTR</b>, free it by calling the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the ASN.1-encoded string that represents the CRL distribution information array.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa383911(v=VS.85).aspx">ICertEncodeCRLDistInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa383969(v=VS.85).aspx">ICertEncodeCRLDistInfo::Reset</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa383982(v=VS.85).aspx">ICertEncodeCRLDistInfo::SetNameCount</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa383985(v=VS.85).aspx">ICertEncodeCRLDistInfo::SetNameEntry</a>
 

 

