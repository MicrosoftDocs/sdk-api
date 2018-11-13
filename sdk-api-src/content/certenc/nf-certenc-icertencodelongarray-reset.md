---
UID: NF:certenc.ICertEncodeLongArray.Reset
title: ICertEncodeLongArray::Reset
author: windows-sdk-content
description: Specifies the size of the array in this object.
old-location: security\icertencodelongarray_reset.htm
tech.root: seccrypto
ms.assetid: 4b5821e0-c81a-47b7-98b0-2a293967d8f6
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: CCertEncodeLongArray object [Security],Reset method, ICertEncodeLongArray interface [Security],Reset method, ICertEncodeLongArray.Reset, ICertEncodeLongArray::Reset, Reset, Reset method [Security], Reset method [Security],CCertEncodeLongArray object, Reset method [Security],ICertEncodeLongArray interface, _certsrv_icertencodelongarray_reset, certenc/ICertEncodeLongArray::Reset, security.icertencodelongarray_reset
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
 - ICertEncodeLongArray.Reset
 - CCertEncodeLongArray.Reset
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertEncodeLongArray::Reset


## -description


The <b>Reset</b> method specifies the size of the array in this object. The values of all the elements in the array are set to zero.
		You must call this method before calling the <a href="https://msdn.microsoft.com/021b2539-3226-4893-af76-9b7b1637e12e">ICertEncodeLongArray::SetValue</a> method for the first time.


## -parameters




### -param Count [in]

Specifies the number of elements in the <b>Long</b> array.


## -returns



<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/e8555282-6c09-4f23-830e-358bc73287ee">ICertEncodeLongArray</a>
 

 

