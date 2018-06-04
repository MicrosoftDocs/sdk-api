---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IDiscFormat2::IsCurrentMediaSupported


## -description


Determines if the current media in a supported recorder supports the given format.


## -parameters




### -param recorder [in]

An <a href="https://msdn.microsoft.com/34f858b8-74eb-4725-8815-7954cb98cff0">IDiscRecorder2</a> interface of the recorder to test.


### -param value [out]

Is VARIANT_TRUE if the media in the recorder supports the given format; otherwise, VARIANT_FALSE.

<div class="alert"><b>Note</b>  VARIANT_TRUE also implies that the result from <a href="https://msdn.microsoft.com/1a96283a-a5a3-434a-834a-d539160cfc5c">IsDiscRecorderSupported</a> is VARIANT_TRUE. </div>
<div> </div>

## -returns



S_OK or S_FALSE are returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer is not valid.

Value: 0x80004003

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_RECORDER_MEDIA_NO_MEDIA</b></dt>
</dl>
</td>
<td width="60%">
There is no media in the device.

(HRESULT)0xC0AA0202

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  Currently, Windows Vista will return<b> S_OK</b> and <b>VARIANT_FALSE</b> when media is not present in the device, while <b> E_IMAPI_RECORDER_MEDIA_NO_MEDIA</b> and <b>VARIANT_FALSE</b> are returned in Windows 7.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/c0bc2e8b-bd60-4c97-bd86-41963b20b1a3">IDiscFormat2</a>



<a href="https://msdn.microsoft.com/1a96283a-a5a3-434a-834a-d539160cfc5c">IDiscFormat2::IsDiscRecorderSupported</a>
 

 

