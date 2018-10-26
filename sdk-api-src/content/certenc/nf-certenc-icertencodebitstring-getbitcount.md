---
UID: NF:certenc.ICertEncodeBitString.GetBitCount
title: ICertEncodeBitString::GetBitCount
author: windows-sdk-content
description: Returns the number of bits in a bit string that belongs to the CertEncodeBitString object and has been initialized by an earlier call to ICertEncodeBitString::Decode.
old-location: security\icertencodebitstring_getbitcount.htm
tech.root: seccrypto
ms.assetid: 9fbaaf03-02b8-4c6f-8cc2-3fd897fdc81d
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: CCertEncodeBitString object [Security],GetBitCount method, GetBitCount, GetBitCount method [Security], GetBitCount method [Security],CCertEncodeBitString object, GetBitCount method [Security],ICertEncodeBitString interface, ICertEncodeBitString interface [Security],GetBitCount method, ICertEncodeBitString.GetBitCount, ICertEncodeBitString::GetBitCount, _certsrv_icertencodebitstring_getbitcount, certenc/ICertEncodeBitString::GetBitCount, security.icertencodebitstring_getbitcount
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
 - ICertEncodeBitString.GetBitCount
 - CCertEncodeBitString.GetBitCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertEncodeBitString::GetBitCount


## -description


The <b>GetBitCount</b> method returns the number of bits in a bit string that belongs to the 
<a href="https://msdn.microsoft.com/51178b67-46da-49f8-9bd7-a500e846e0a8">CertEncodeBitString</a> object and has been initialized by an earlier call to 
<a href="https://msdn.microsoft.com/65856db4-97db-4c9b-ac12-1a9262c7b4e9">ICertEncodeBitString::Decode</a>.


## -parameters




### -param pBitCount [out]

A pointer to a <b>Long</b> that will receive the number of bits in the bit string.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the number of bits in the bit string.




## -see-also




<a href="https://msdn.microsoft.com/51178b67-46da-49f8-9bd7-a500e846e0a8">ICertEncodeBitString</a>
 

 

