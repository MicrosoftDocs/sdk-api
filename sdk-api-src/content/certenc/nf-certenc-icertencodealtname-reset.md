---
UID: NF:certenc.ICertEncodeAltName.Reset
title: ICertEncodeAltName::Reset
author: windows-sdk-content
description: Specifies the size of the alternate name array in this object. The value of all elements in the array are set to zero.
old-location: security\icertencodealtname_reset.htm
old-project: SecCrypto
ms.assetid: 99aa43fe-534b-4696-8bfc-7049b16be1cf
ms.author: windowssdkdev
ms.date: 08/15/2018
ms.keywords: CCertEncodeAltName object [Security],Reset method, ICertEncodeAltName interface [Security],Reset method, ICertEncodeAltName.Reset, ICertEncodeAltName::Reset, Reset, Reset method [Security], Reset method [Security],CCertEncodeAltName object, Reset method [Security],ICertEncodeAltName interface, certenc/ICertEncodeAltName::Reset, security.icertencodealtname_reset
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: certenc.h
req.include-header: Certsrv.h
req.redist: 
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
 - ICertEncodeAltName.Reset
 - CCertEncodeAltName.Reset
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certenc.dll
req.irql: 
---

# ICertEncodeAltName::Reset


## -description


The <b>Reset</b> method specifies the size of the alternate name array in this object. The value of all elements in the array are set to zero.


## -parameters




### -param NameCount [in]

Specifies the number of elements in the array.


## -returns



<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/e0ecfcb0-f2ca-4e1c-a054-c83c03d55465">ICertEncodeAltName</a>
 

 

