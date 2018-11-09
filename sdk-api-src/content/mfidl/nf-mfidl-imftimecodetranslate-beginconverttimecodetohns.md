---
UID: NF:mfidl.IMFTimecodeTranslate.BeginConvertTimecodeToHNS
title: IMFTimecodeTranslate::BeginConvertTimecodeToHNS
author: windows-sdk-content
description: Starts an asynchronous call to convert Society of Motion Picture and Television Engineers (SMPTE) time code to 100-nanosecond units.
old-location: mf\imftimecodetranslate_beginconverttimecodetohns.htm
tech.root: medfound
ms.assetid: 4e25d5e4-b4d7-4ca4-81c9-12c6d712322d
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: BeginConvertTimecodeToHNS, BeginConvertTimecodeToHNS method [Media Foundation], BeginConvertTimecodeToHNS method [Media Foundation],IMFTimecodeTranslate interface, IMFTimecodeTranslate interface [Media Foundation],BeginConvertTimecodeToHNS method, IMFTimecodeTranslate.BeginConvertTimecodeToHNS, IMFTimecodeTranslate::BeginConvertTimecodeToHNS, mf.imftimecodetranslate_beginconverttimecodetohns, mfidl/IMFTimecodeTranslate::BeginConvertTimecodeToHNS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - mfidl.h
api_name:
 - IMFTimecodeTranslate.BeginConvertTimecodeToHNS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFTimecodeTranslate::BeginConvertTimecodeToHNS


## -description


Starts an asynchronous call to convert Society of Motion Picture and Television Engineers (SMPTE) time code to 100-nanosecond units.


## -parameters




### -param pPropVarTimecode [in]

Time in SMPTE time code to convert. The <b>vt</b> member of the <b>PROPVARIANT</b> structure is set to <b>VT_I8</b>. The <b>hVal.QuadPart</b> member contains the time in binary coded decimal (BCD) form. See Remarks.


### -param pCallback [in]

Pointer to the <a href="https://msdn.microsoft.com/7edff985-da59-4cc0-96de-1a92e03a7d41">IMFAsyncCallback</a> interface of a callback object. The caller must implement this interface.


### -param punkState [in]

PPointer to the <b>IUnknown</b> interface of a state object, defined by the caller. This parameter can be <b>NULL</b>. You can use this object to hold state information. The object is returned to the caller when the callback is invoked.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pPropVarTimecode</i> is not <b>VT_I8</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The object's <b>Shutdown</b> method was called.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_BYTESTREAM_NOT_SEEKABLE</b></dt>
</dl>
</td>
<td width="60%">
The byte stream is not seekable. The time code cannot be read from the end of the byte stream.

</td>
</tr>
</table>
 




## -remarks



When the asynchronous method completes, the callback object's <a href="https://msdn.microsoft.com/22473605-637e-4783-a8cb-98248b0a0327">IMFAsyncCallback::Invoke</a> method is called. At that point, the application must call <a href="https://msdn.microsoft.com/d1b8b8ba-d03a-4a45-8788-38dbb2be8c6a">IMFTimecodeTranslate::EndConvertTimecodeToHNS</a> to complete the asynchronous request.

The value of <i>pPropVarTimecode</i> is a 64-bit unsigned value typed as a <b>LONGLONG</b>. The upper <b>DWORD</b> contains the range. (A <i>range</i> is a continuous series of time codes.) The lower <b>DWORD</b> contains the time code in the form of a hexadecimal number <i>0xhhmmssff</i>,  where each 2-byte sequence is read as a decimal value.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>void CreateTimeCode(
    DWORD dwFrames,
    DWORD dwSeconds,
    DWORD dwMinutes,
    DWORD dwHours,
    DWORD dwRange,
    PROPVARIANT *pvar
    )
{
    ULONGLONG ullTimecode = ((ULONGLONG)dwRange) &lt;&lt; 32;

    ullTimecode +=   dwFrames  % 10;
    ullTimecode += (( (ULONGLONG)dwFrames )  / 10) &lt;&lt; 4;
    ullTimecode += (( (ULONGLONG)dwSeconds ) % 10) &lt;&lt; 8;
    ullTimecode += (( (ULONGLONG)dwSeconds ) / 10) &lt;&lt; 12;
    ullTimecode += (( (ULONGLONG)dwMinutes ) % 10) &lt;&lt; 16;
    ullTimecode += (( (ULONGLONG)dwMinutes ) / 10) &lt;&lt; 20;
    ullTimecode += (( (ULONGLONG)dwHours )   % 10) &lt;&lt; 24;
    ullTimecode += (( (ULONGLONG)dwHours )   / 10) &lt;&lt; 28;

    pvar-&gt;vt = VT_I8;
    pvar-&gt;hVal.QuadPart = (LONGLONG)ullTimecode;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/1d8688a5-d476-457d-a0ad-e4f106ac3484">Calling Asynchronous Methods</a>



<a href="https://msdn.microsoft.com/935ec6b3-12e6-4458-b8a1-ffeb4159d957">IMFTimecodeTranslate</a>
 

 

