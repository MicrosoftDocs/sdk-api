---
UID: NF:certenc.ICertEncodeLongArray.GetCount
title: ICertEncodeLongArray::GetCount
author: windows-sdk-content
description: Returns the number of Long values in the object's Long array.
old-location: security\icertencodelongarray_getcount.htm
tech.root: seccrypto
ms.assetid: f60cffb1-5202-4dc8-97dd-9eddd381602a
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: CCertEncodeLongArray object [Security],GetCount method, GetCount, GetCount method [Security], GetCount method [Security],CCertEncodeLongArray object, GetCount method [Security],ICertEncodeLongArray interface, ICertEncodeLongArray interface [Security],GetCount method, ICertEncodeLongArray.GetCount, ICertEncodeLongArray::GetCount, _certsrv_icertencodelongarray_getcount, certenc/ICertEncodeLongArray::GetCount, security.icertencodelongarray_getcount
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
 - ICertEncodeLongArray.GetCount
 - CCertEncodeLongArray.GetCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- certenc.h
: 
- ICertEncodeLongArray.GetCount
: 
---

# ICertEncodeLongArray::GetCount


## -description


The <b>GetCount</b> method returns the number of <b>Long</b> values in the object's <b>Long</b> array.


## -parameters




### -param pCount [out]

A pointer to a <b>Long</b> that receives the number of <b>Long</b> values contained in the <b>Long</b> array.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.

<h3>VB</h3>
The return value is the number of <b>Long</b> values contained in the <b>Long</b> array.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa384997(v=VS.85).aspx">ICertEncodeLongArray</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa385010(v=VS.85).aspx">ICertEncodeLongArray::Reset</a>
 

 

