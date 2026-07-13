---
UID: NF:msacm.acmFormatEnumA
title: acmFormatEnumA function (msacm.h)
description: The acmFormatEnum function enumerates waveform-audio formats available for a given format tag from an ACM driver. This function continues enumerating until there are no more suitable formats for the format tag or the callback function returns FALSE. (acmFormatEnumA)
helpviewer_keywords: ["acmFormatEnumA", "msacm/acmFormatEnumA"]
old-location: multimedia\acmformatenum.htm
tech.root: Multimedia
ms.assetid: 31da0e86-a298-4ef6-a515-4954aa120656
ms.date: 12/05/2018
ms.keywords: _win32_acmFormatEnum, acmFormatEnum, acmFormatEnum function [Windows Multimedia], acmFormatEnumA, acmFormatEnumW, msacm/acmFormatEnum, msacm/acmFormatEnumA, msacm/acmFormatEnumW, multimedia.acmformatenum
req.header: msacm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: acmFormatEnumW (Unicode) and acmFormatEnumA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Msacm32.lib
req.dll: Msacm32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - acmFormatEnumA
 - msacm/acmFormatEnumA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msacm32.dll
 - Ext-MS-Win-mm-msacm-l1-1-0.dll
api_name:
 - acmFormatEnum
 - acmFormatEnumA
 - acmFormatEnumW
---

# acmFormatEnumA function


## -description

The <b>acmFormatEnum</b> function enumerates waveform-audio formats available for a given format tag from an ACM driver. This function continues enumerating until there are no more suitable formats for the format tag or the callback function returns <b>FALSE</b>.

## -parameters

### -param had

Handle to the ACM driver to query for waveform-audio format details. If this parameter is <b>NULL</b>, the ACM uses the details from the first suitable ACM driver.

### -param pafd

Pointer to an [ACMFORMATDETAILS](./nf-msacm-acmformatdetails.md) structure to contain the format details passed to the <b>fnCallback</b> function. This structure must have the <b>cbStruct</b>, <b>pwfx</b>, and <b>cbwfx</b> members of the <b>ACMFORMATDETAILS</b> structure initialized. The <b>dwFormatTag</b> member must also be initialized to either WAVE_FORMAT_UNKNOWN or a valid format tag.

The <b>fdwSupport</b> member of the structure must be initialized to zero.

To find the required size of the <b>pwfx</b> buffer, call <a href="/windows/desktop/api/msacm/nf-msacm-acmmetrics">acmMetrics</a> with the ACM_METRIC_MAX_SIZE_FORMAT flag.

### -param fnCallback

Address of an application-defined callback function. See <a href="/windows/desktop/api/msacm/nc-msacm-acmformatenumcb">acmFormatEnumCallback</a>. This parameter cannot be <b>NULL</b>.

### -param dwInstance

A 64-bit (DWORD_PTR) or 32-bit (DWORD) application-defined value that is passed to the callback function along with ACM format details.

### -param fdwEnum

Flags for enumerating the formats for a given format tag. The following values are defined.

<table>
<tr>
<th>Value
</th>
<th>Meaning
</th>
</tr>
<tr>
<td>ACM_FORMATENUMF_CONVERT</td>
[ACMFORMATDETAILS](./nf-msacm-acmformatdetails.md) structure is valid. The enumerator will only enumerate destination formats that can be converted from the given <b>pwfx</b> format.If this flag is used, the <b>wFormatTag</b> member of the <b>WAVEFORMATEX</b> structure cannot be WAVE_FORMAT_UNKNOWN.

</td>
</tr>
<tr>
<td>ACM_FORMATENUMF_HARDWARE</td>
<td>The enumerator should only enumerate formats that are supported as native input or output formats on one or more of the installed waveform-audio devices. This flag provides a way for an application to choose only formats native to an installed waveform-audio device. This flag must be used with one or both of the ACM_FORMATENUMF_INPUT and ACM_FORMATENUMF_OUTPUT flags. Specifying both ACM_FORMATENUMF_INPUT and ACM_FORMATENUMF_OUTPUT will enumerate only formats that can be opened for input or output. This is true regardless of whether this flag is specified.</td>
</tr>
<tr>
<td>ACM_FORMATENUMF_INPUT</td>
<td>Enumerator should enumerate only formats that are supported for input (recording).</td>
</tr>
<tr>
<td>ACM_FORMATENUMF_NCHANNELS</td>
[ACMFORMATDETAILS](./nf-msacm-acmformatdetails.md) structure is valid. The enumerator will enumerate only a format that conforms to this attribute.</td>
</tr>
<tr>
<td>ACM_FORMATENUMF_NSAMPLESPERSEC</td>
<td>The <b>nSamplesPerSec</b> member of the <b>WAVEFORMATEX</b> structure pointed to by the <b>pwfx</b> member of the <b>ACMFORMATDETAILS</b> structure is valid. The enumerator will enumerate only a format that conforms to this attribute.</td>
</tr>
<tr>
<td>ACM_FORMATENUMF_OUTPUT</td>
<td>Enumerator should enumerate only formats that are supported for output (playback).</td>
</tr>
<tr>
<td>ACM_FORMATENUMF_SUGGEST</td>
[ACMFORMATDETAILS](./nf-msacm-acmformatdetails.md) structure is valid. The enumerator will enumerate all suggested destination formats for the given <b>pwfx</b> format. This mechanism can be used instead of the <a href="/windows/desktop/api/msacm/nf-msacm-acmformatsuggest">acmFormatSuggest</a> function to allow an application to choose the best suggested format for conversion. The <b>dwFormatIndex</b> member will always be set to zero on return.If this flag is used, the <b>wFormatTag</b> member of the <b>WAVEFORMATEX</b> structure cannot be WAVE_FORMAT_UNKNOWN.

</td>
</tr>
<tr>
<td>ACM_FORMATENUMF_WBITSPERSAMPLE</td>
<td>The <b>wBitsPerSample</b> member of the <b>WAVEFORMATEX</b> structure pointed to by the <b>pwfx</b> member of the <b>ACMFORMATDETAILS</b> structure is valid. The enumerator will enumerate only a format that conforms to this attribute.</td>
</tr>
<tr>
<td>ACM_FORMATENUMF_WFORMATTAG</td>
<td>The <b>wFormatTag</b> member of the <b>WAVEFORMATEX</b> structure pointed to by the <b>pwfx</b> member of the <b>ACMFORMATDETAILS</b> structure is valid. The enumerator will enumerate only a format that conforms to this attribute. The <b>dwFormatTag</b> member of the <b>ACMFORMATDETAILS</b> structure must be equal to the <b>wFormatTag</b> member.The value of <b>wFormatTag</b> cannot be WAVE_FORMAT_UNKNOWN in this case.

</td>
</tr>
</table>

## -returns

Returns zero if successful or an error otherwise. Possible error values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ACMERR_NOTPOSSIBLE</b></dt>
</dl>
</td>
<td width="60%">
The details for the format cannot be returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_INVALFLAG</b></dt>
</dl>
</td>
<td width="60%">
At least one flag is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_INVALHANDLE</b></dt>
</dl>
</td>
<td width="60%">
The specified handle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_INVALPARAM</b></dt>
</dl>
</td>
<td width="60%">
At least one parameter is invalid.

</td>
</tr>
</table>

## -remarks

This function will return MMSYSERR_NOERROR (zero) if no suitable ACM drivers are installed. Moreover, the callback function will not be called.


#### Examples

The following example shows how to enumerate formats that have the WAVE_FORMAT_MPEGLAYER3 format tag.


```cpp

MMRESULT EnumerateMP3Codecs()
{
    DWORD cbMaxSize = 0;
    MMRESULT result = MMSYSERR_NOERROR;
    ACMFORMATDETAILS acmFormatDetails;

    // Buffer to hold the format information.
    BYTE *pFormat = NULL;   // Caller allocated.

    // Find the largest format buffer needed.
    result = acmMetrics(NULL, ACM_METRIC_MAX_SIZE_FORMAT, &cbMaxSize);
    if (result != MMSYSERR_NOERROR)
    {
        return result;
    }

    // Allocate the format buffer.
    pFormat = new BYTE[cbMaxSize];
    if (pFormat == NULL)
    {
        return MMSYSERR_NOMEM;
    }

    ZeroMemory(pFormat, cbMaxSize);

    // Ask for WAVE_FORMAT_MPEGLAYER3 formats.
    WAVEFORMATEX* pWaveFormat = (WAVEFORMATEX*)pFormat;
    pWaveFormat->wFormatTag = WAVE_FORMAT_MPEGLAYER3;

    // Set up the acmFormatDetails structure.
    ZeroMemory(&acmFormatDetails, sizeof(acmFormatDetails));
    acmFormatDetails.cbStruct = sizeof(ACMFORMATDETAILS);
    acmFormatDetails.pwfx = pWaveFormat; 
    acmFormatDetails.cbwfx = cbMaxSize;

    // For the ACM_FORMATENUMF_WFORMATTAG request, the format
    // tag in acmFormatDetails must match the format tag in
    // the pFormat buffer.
    acmFormatDetails.dwFormatTag = WAVE_FORMAT_MPEGLAYER3;

    result = acmFormatEnum(NULL, &acmFormatDetails, acmFormatEnumCallback,
        0, ACM_FORMATENUMF_WFORMATTAG);

    delete [] pFormat;

    return result;
}

```


The next example shows the callback function for the previous example. The callback function is called once for each matching format or until the callback returns <b>FALSE</b>.


```cpp

BOOL CALLBACK acmFormatEnumCallback(
  HACMDRIVERID       hadid,      
  LPACMFORMATDETAILS pafd,       
  DWORD_PTR          dwInstance, 
  DWORD              fdwSupport  
)
{
    BOOL bContinue = TRUE;
    MPEGLAYER3WAVEFORMAT *pMP3WaveFormat = NULL;

    if (pafd->pwfx->wFormatTag == WAVE_FORMAT_MPEGLAYER3)
    {
        pMP3WaveFormat = (MPEGLAYER3WAVEFORMAT*)pafd->pwfx;

        // TODO: Examine the format. 

        // To halt the enumeration, set bContinue to FALSE.
    }


    return bContinue;
}

```






> [!NOTE]
> The msacm.h header defines acmFormatEnum as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Multimedia/audio-compression-functions">Audio Compression Functions</a>



<a href="/windows/desktop/Multimedia/audio-compression-manager">Audio Compression Manager</a>
