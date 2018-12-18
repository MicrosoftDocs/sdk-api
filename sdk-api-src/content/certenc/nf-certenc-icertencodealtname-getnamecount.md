---
UID: NF:certenc.ICertEncodeAltName.GetNameCount
title: ICertEncodeAltName::GetNameCount
author: windows-sdk-content
description: Returns the number of names in the alternate name array.
old-location: security\icertencodealtname_getnamecount.htm
tech.root: seccrypto
ms.assetid: 3f5e5c5d-e21b-452b-837c-5b44daa884b8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CCertEncodeAltName object [Security],GetNameCount method, GetNameCount, GetNameCount method [Security], GetNameCount method [Security],CCertEncodeAltName object, GetNameCount method [Security],ICertEncodeAltName interface, ICertEncodeAltName interface [Security],GetNameCount method, ICertEncodeAltName.GetNameCount, ICertEncodeAltName::GetNameCount, _certsrv_icertencodealtname_getnamecount, certenc/ICertEncodeAltName::GetNameCount, security.icertencodealtname_getnamecount
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
 - ICertEncodeAltName.GetNameCount
 - CCertEncodeAltName.GetNameCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertEncodeAltName::GetNameCount


## -description


The <b>GetNameCount</b> method returns the number of names in the  alternate name array.


## -parameters




### -param pNameCount [out]

The number of alternate names in the array.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the number of alternate names in the array.




## -see-also




<a href="https://msdn.microsoft.com/e0ecfcb0-f2ca-4e1c-a054-c83c03d55465">ICertEncodeAltName</a>
 

 

