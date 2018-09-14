---
UID: NF:amstream.IAMMediaTypeSample.SetActualDataLength
title: IAMMediaTypeSample::SetActualDataLength
author: windows-sdk-content
description: Note  This interface is deprecated. New applications should not use it. The SetActualDataLength method sets the sample's data length.
old-location: dshow\iammediatypesample_setactualdatalength.htm
tech.root: DirectShow
ms.assetid: 158a1761-7d42-4611-9667-9e717b23a2da
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IAMMediaTypeSample interface [DirectShow],SetActualDataLength method, IAMMediaTypeSample.SetActualDataLength, IAMMediaTypeSample::SetActualDataLength, IAMMediaTypeSampleSetActualDataLength, SetActualDataLength, SetActualDataLength method [DirectShow], SetActualDataLength method [DirectShow],IAMMediaTypeSample interface, amstream/IAMMediaTypeSample::SetActualDataLength, dshow.iammediatypesample_setactualdatalength
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: amstream.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - amstream.h
api_name:
 - IAMMediaTypeSample.SetActualDataLength
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMMediaTypeSample::SetActualDataLength


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>SetActualDataLength</code> method sets the sample's data length.




## -parameters




### -param __MIDL__IAMMediaTypeSample0000

TBD




#### - lActual

Length of the data in the media sample, in bytes.


## -returns



Returns one of the following values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_BUFFER_OVERFLOW</b></dt>
</dl>
</td>
<td width="60%">
The buffer is not big enough.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/e0a62251-68ee-4318-b09a-0aac6b73bf54">IAMMediaTypeSample Interface</a>
 

 

