---
UID: NF:mfidl.IMFTimecodeTranslate.EndConvertHNSToTimecode
title: IMFTimecodeTranslate::EndConvertHNSToTimecode
author: windows-sdk-content
description: Completes an asynchronous request to convert time in 100-nanosecond units to Society of Motion Picture and Television Engineers (SMPTE) time code.
old-location: mf\imftimecodetranslate_endconverthnstotimecode.htm
tech.root: MedFound
ms.assetid: 9386748c-e551-49b8-89c3-65d721820736
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: EndConvertHNSToTimecode, EndConvertHNSToTimecode method [Media Foundation], EndConvertHNSToTimecode method [Media Foundation],IMFTimecodeTranslate interface, IMFTimecodeTranslate interface [Media Foundation],EndConvertHNSToTimecode method, IMFTimecodeTranslate.EndConvertHNSToTimecode, IMFTimecodeTranslate::EndConvertHNSToTimecode, mf.imftimecodetranslate_endconverthnstotimecode, mfidl/IMFTimecodeTranslate::EndConvertHNSToTimecode
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
 - IMFTimecodeTranslate.EndConvertHNSToTimecode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFTimecodeTranslate::EndConvertHNSToTimecode


## -description


Completes an asynchronous request to convert time in 100-nanosecond units to Society of Motion Picture and Television Engineers (SMPTE) time code.


## -parameters




### -param pResult [in]

A pointer to the <a href="https://msdn.microsoft.com/8c95b1de-8974-445c-8070-41552ea83e53">IMFAsyncResult</a> interface. Pass in the same pointer that your callback object received in the <a href="https://msdn.microsoft.com/22473605-637e-4783-a8cb-98248b0a0327">IMFAsyncCallback::Invoke</a> method.


### -param pPropVarTimecode [out]

A pointer to a <b>PROPVARIANT</b> that receives the converted time. The <b>vt</b> member of the <b>PROPVARIANT</b> structure is set to VT_I8. The <b>hVal.QuadPart</b> member contains the converted time in binary coded decimal (BCD) form. See Remarks.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Call this method after the <a href="https://msdn.microsoft.com/42b5de27-aaa6-4bd9-b2b0-3aeabfc28ef2">IMFTimecodeTranslate::BeginConvertHNSToTimecode</a> method completes asynchronously.

The value of <i>pPropVarTimecode</i> is a 64-bit unsigned value typed as a <b>LONGLONG</b>. The upper <b>DWORD</b> contains the range. (A <i>range</i> is a continuous series of time codes.) The lower <b>DWORD</b> contains the time code in the form of a hexadecimal number <i>0xhhmmssff</i>,  where each 2-byte sequence is read as a decimal value.


```cpp
HRESULT ParseTimeCode(
    const PROPVARIANT& var,
    DWORD *pdwRange,
    DWORD *pdwFrames,
    DWORD *pdwSeconds,
    DWORD *pdwMinutes,
    DWORD *pdwHours
    )
{
    if (var.vt != VT_I8)
    {
        return E_INVALIDARG;
    }

    ULONGLONG ullTimeCode = (ULONGLONG)var.hVal.QuadPart;
    DWORD dwTimecode = (DWORD)(ullTimeCode & 0xFFFFFFFF);

    *pdwRange   = (DWORD)(ullTimeCode >> 32);
    *pdwFrames  =     dwTimecode & 0x0000000F;
    *pdwFrames  += (( dwTimecode & 0x000000F0) >> 4 )  * 10;
    *pdwSeconds =   ( dwTimecode & 0x00000F00) >> 8;
    *pdwSeconds += (( dwTimecode & 0x0000F000) >> 12 ) * 10;
    *pdwMinutes =   ( dwTimecode & 0x000F0000) >> 16;
    *pdwMinutes += (( dwTimecode & 0x00F00000) >> 20 ) * 10;
    *pdwHours   =   ( dwTimecode & 0x0F000000) >> 24;
    *pdwHours   += (( dwTimecode & 0xF0000000) >> 28 ) * 10;

    return S_OK;
}

```





## -see-also




<a href="https://msdn.microsoft.com/1d8688a5-d476-457d-a0ad-e4f106ac3484">Calling Asynchronous Methods</a>



<a href="https://msdn.microsoft.com/935ec6b3-12e6-4458-b8a1-ffeb4159d957">IMFTimecodeTranslate</a>
 

 

