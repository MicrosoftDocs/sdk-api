---
UID: NF:certenc.ICertEncodeAltName.Decode
title: ICertEncodeAltName::Decode
author: windows-sdk-content
description: Decodes an Abstract Syntax Notation One (ASN.1)-encoded alternate name extension and stores the resulting array of strings in the CertEncodeAltName object.
old-location: security\icertencodealtname_decode.htm
tech.root: seccrypto
ms.assetid: 0507d3a5-b8c3-4f2e-996f-e1e32957f475
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: CCertEncodeAltName object [Security],Decode method, Decode, Decode method [Security], Decode method [Security],CCertEncodeAltName object, Decode method [Security],ICertEncodeAltName interface, ICertEncodeAltName interface [Security],Decode method, ICertEncodeAltName.Decode, ICertEncodeAltName::Decode, _certsrv_icertencodealtname_decode, certenc/ICertEncodeAltName::Decode, security.icertencodealtname_decode
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
 - ICertEncodeAltName.Decode
 - CCertEncodeAltName.Decode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertEncodeAltName::Decode


## -description


The <b>Decode</b> method decodes an <a href="https://msdn.microsoft.com/en-us/library/ms721532(v=VS.85).aspx">Abstract Syntax Notation One</a> (ASN.1)-encoded alternate name extension and stores the resulting array of strings in the <b>CertEncodeAltName</b> object.


## -parameters




### -param strBinary [in]

Represents an ASN.1-encoded alternate name extension.


## -returns



<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa383295(v=VS.85).aspx">ICertEncodeAltName</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa383302(v=VS.85).aspx">ICertEncodeAltName::Encode</a>
 

 

