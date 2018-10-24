---
UID: NF:msacm.acmFilterEnumA
title: acmFilterEnumA function
author: windows-sdk-content
description: The acmFilterEnum function enumerates waveform-audio filters available for a given filter tag from an ACM driver. This function continues enumerating until there are no more suitable filters for the filter tag or the callback function returns FALSE.
old-location: multimedia\acmfilterenum.htm
tech.root: Multimedia
ms.assetid: ee8154d6-3aa1-49ce-96c5-7b8526f02a8a
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: "_win32_acmFilterEnum, acmFilterEnum, acmFilterEnum function [Windows Multimedia], acmFilterEnumA, acmFilterEnumW, msacm/acmFilterEnum, msacm/acmFilterEnumA, msacm/acmFilterEnumW, multimedia.acmfilterenum"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: msacm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: acmFilterEnumW (Unicode) and acmFilterEnumA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Msacm32.lib
req.dll: Msacm32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msacm32.dll
 - Ext-MS-Win-mm-msacm-l1-1-0.dll
api_name:
 - acmFilterEnum
 - acmFilterEnumA
 - acmFilterEnumW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# acmFilterEnumA function


## -description



The <b>acmFilterEnum</b> function enumerates waveform-audio filters available for a given filter tag from an ACM driver. This function continues enumerating until there are no more suitable filters for the filter tag or the callback function returns <b>FALSE</b>.




## -parameters




### -param had

Handle to the ACM driver to query for waveform-audio filter details. If this parameter is <b>NULL</b>, the ACM uses the details from the first suitable ACM driver.


### -param pafd

Pointer to the <a href="https://msdn.microsoft.com/c0423701-b957-4f77-a565-f6f761614389">ACMFILTERDETAILS</a> structure that contains the filter details when it is passed to the function specified by <i>fnCallback</i>. When your application calls <b>acmFilterEnum</b>, the <b>cbStruct</b>, <b>pwfltr</b>, and <b>cbwfltr</b> members of this structure must be initialized. The <b>dwFilterTag</b> member must also be initialized to either WAVE_FILTER_UNKNOWN or a valid filter tag.


### -param fnCallback

Procedure-instance address of the application-defined callback function.


### -param dwInstance

A 32-bit (DWORD), 64-bit (DWORD_PTR) application-defined value that is passed to the callback function along with ACM filter details.


### -param fdwEnum

Flags for enumerating the filters for a given filter tag. The following values are defined.

<table>
<tr>
<th>Value
</th>
<th>Meaning
</th>
</tr>
<tr>
<td>ACM_FILTERENUMF_DWFILTERTAG</td>
<td>The <b>dwFilterTag</b> member of the <a href="https://msdn.microsoft.com/dea3df47-88a2-439f-bf07-b5c592bf23e8">WAVEFILTER</a> structure pointed to by the <b>pwfltr</b> member of the <a href="https://msdn.microsoft.com/c0423701-b957-4f77-a565-f6f761614389">ACMFILTERDETAILS</a> structure is valid. The enumerator will enumerate only a filter that conforms to this attribute. The <b>dwFilterTag</b> member of the <b>ACMFILTERDETAILS</b> structure must be equal to the <b>dwFilterTag</b> member of the <b>WAVEFILTER</b> structure.</td>
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
The details for the filter cannot be returned.

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



The <b>acmFilterEnum</b> function will return MMSYSERR_NOERROR (zero) if no suitable ACM drivers are installed. Moreover, the callback function will not be called.

The following functions should not be called from within the callback function: <b>acmDriverAdd</b>, <b>acmDriverRemove</b>, and <b>acmDriverPriority</b>.




## -see-also




<a href="https://msdn.microsoft.com/da207a50-9c67-4cf3-920b-5878637060db">Audio Compression Functions</a>



<a href="https://msdn.microsoft.com/2f9a4540-86c0-40e6-b4da-24a9d31b56bf">Audio Compression Manager</a>
 

 

