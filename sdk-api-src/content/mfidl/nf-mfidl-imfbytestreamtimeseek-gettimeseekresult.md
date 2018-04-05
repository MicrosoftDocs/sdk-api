---
UID: NF:mfidl.IMFByteStreamTimeSeek.GetTimeSeekResult
title: IMFByteStreamTimeSeek::GetTimeSeekResult method
author: windows-driver-content
description: Gets the result of a time-based seek.
old-location: mf\imfbytestreamtimeseek_gettimeseekresult.htm
old-project: medfound
ms.assetid: D56E1F06-AA05-430C-BF5C-30B38831B842
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: GetTimeSeekResult method [Media Foundation], GetTimeSeekResult method [Media Foundation], IMFByteStreamTimeSeek interface, GetTimeSeekResult,IMFByteStreamTimeSeek.GetTimeSeekResult, IMFByteStreamTimeSeek, IMFByteStreamTimeSeek interface [Media Foundation], GetTimeSeekResult method, IMFByteStreamTimeSeek::GetTimeSeekResult, mf.imfbytestreamtimeseek_gettimeseekresult, mfidl/IMFByteStreamTimeSeek::GetTimeSeekResult
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfidl.h
api_name:
-	IMFByteStreamTimeSeek.GetTimeSeekResult
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFByteStreamTimeSeek::GetTimeSeekResult method


## -description


Gets the result of a time-based seek.


## -parameters




### -param pqwStartTime [out]

Receives the new position after the seek, in 100-nanosecond units.


### -param pqwStopTime [out]

Receives the stop time, in 100-nanosecond units. If the stop time is unknown, the value is zero.


### -param pqwDuration [out]

Receives the total duration of the file, in 100-nanosecond units. If the duration is unknown, the value is –1.


## -returns



This method can return one of these values.

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
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
The byte stream does not support time-based seeking, or no data is available.

</td>
</tr>
</table>
 




## -remarks



This method returns the server response from a previous time-based seek. 

<div class="alert"><b>Note</b>  This method normally cannot be invoked until some data
    is read from the byte stream, because the <a href="https://msdn.microsoft.com/786F1299-A9E2-4B2C-A6AE-F88E6BF022DC">IMFByteStreamTimeSeek::TimeSeek</a>       method does not send a server request immediately.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/BD9EDFF7-46BA-4788-A44E-C69C4B0BEB50">IMFByteStreamTimeSeek</a>
 

 

