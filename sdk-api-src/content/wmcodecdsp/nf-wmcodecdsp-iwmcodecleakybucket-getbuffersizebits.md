---
UID: NF:wmcodecdsp.IWMCodecLeakyBucket.GetBufferSizeBits
title: IWMCodecLeakyBucket::GetBufferSizeBits
author: windows-sdk-content
description: Retrieves the current size of the buffer in bits.
old-location: mf\iwmcodecleakybucketgetbuffersizebits.htm
tech.root: medfound
ms.assetid: 7fa0835e-7386-4032-a94b-ef52259aeea9
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: GetBufferSizeBits, GetBufferSizeBits method [Media Foundation], GetBufferSizeBits method [Media Foundation],IWMCodecLeakyBucket interface, IWMCodecLeakyBucket interface [Media Foundation],GetBufferSizeBits method, IWMCodecLeakyBucket.GetBufferSizeBits, IWMCodecLeakyBucket::GetBufferSizeBits, codecapi.iwmcodecleakybucketgetbuffersizebits, mf.iwmcodecleakybucketgetbuffersizebits, wmcodecdsp/IWMCodecLeakyBucket::GetBufferSizeBits
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmcodecdsp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmcodecdsp.h
api_name:
 - IWMCodecLeakyBucket.GetBufferSizeBits
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMCodecLeakyBucket::GetBufferSizeBits


## -description


Retrieves the current size of the buffer in bits.



## -parameters




### -param pulBufferSize [out]

Pointer to a variable containing the buffer size, in bits.


## -returns



This method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



The buffer size is equal to the bit rate of the stream multiplied by the buffer window. For example, a stream with a bit rate of 28 kilobits per second with a buffer window of 3 seconds would have a buffer of 28000 bits per second x 3 seconds = 84000 bits.




## -see-also




<a href="https://msdn.microsoft.com/93a0169e-39fe-4152-8698-72a0650be41a">IWMCodecLeakyBucket Interface</a>



<a href="https://msdn.microsoft.com/b602e8ca-8446-4f94-bcd0-193084d96565">IWMCodecLeakyBucket::SetBufferSizeBits</a>
 

 

