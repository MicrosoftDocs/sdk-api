---
UID: NF:certenc.ICertEncodeStringArray.GetCount
title: ICertEncodeStringArray::GetCount
author: windows-driver-content
description: Returns the number of string values in the string array.
old-location: security\icertencodestringarray_getcount.htm
old-project: SecCrypto
ms.assetid: c02a23ea-87c2-4458-8b1a-b010e8103a90
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: CCertEncodeStringArray object [Security],GetCount method, GetCount, GetCount method [Security], GetCount method [Security],CCertEncodeStringArray object, GetCount method [Security],ICertEncodeStringArray interface, ICertEncodeStringArray interface [Security],GetCount method, ICertEncodeStringArray.GetCount, ICertEncodeStringArray::GetCount, _certsrv_icertencodestringarray_getcount, certenc/ICertEncodeStringArray::GetCount, security.icertencodestringarray_getcount
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
req.typenames: X509EnrollmentAuthFlags
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Certenc.dll
api_name:
-	ICertEncodeStringArray.GetCount
-	CCertEncodeStringArray.GetCount
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certenc.dll
req.irql: 
---

# ICertEncodeStringArray::GetCount


## -description


The <b>GetCount</b> method returns the number of string values in the string array.


## -parameters




### -param pCount [out]

A pointer to a <b>LONG</b> that receives the number of string values contained in the string array.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the number of string values contained in the string array.




## -see-also




<a href="https://msdn.microsoft.com/5515c25e-f788-4222-8f66-f5d86bd2a3a3">ICertEncodeStringArray</a>



<a href="https://msdn.microsoft.com/125524ae-236d-4507-9c00-76a016bf6c62">ICertEncodeStringArray::Reset</a>
 

 

