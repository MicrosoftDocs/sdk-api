---
UID: NC:msacm.ACMDRIVERENUMCB
title: ACMDRIVERENUMCB
author: windows-sdk-content
description: The acmDriverEnumCallback function specifies a callback function used with the acmDriverEnum function. The acmDriverEnumCallback name is a placeholder for an application-defined function name.
old-location: multimedia\acmdriverenumcallback.htm
tech.root: Multimedia
ms.assetid: 8566fd31-ec0c-4325-b182-4765e81c7884
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: ACMDRIVERENUMCB, ACMDRIVERENUMCB callback, ACMDRIVERENUMCB callback function [Windows Multimedia], _win32_acmDriverEnumCallback, acmDriverEnumCallback, msacm/ACMDRIVERENUMCB, multimedia.acmdriverenumcallback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: msacm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - UserDefined
api_location:
 - Msacm.h
api_name:
 - ACMDRIVERENUMCB
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ACMDRIVERENUMCB callback function


## -description



The <b>acmDriverEnumCallback</b> function specifies a callback function used with the <a href="https://msdn.microsoft.com/3e93284d-2810-4c8e-9619-1989d8bf788e">acmDriverEnum</a> function. The <b>acmDriverEnumCallback</b> name is a placeholder for an application-defined function name.




## -parameters




### -param hadid

Handle to an ACM driver identifier.


### -param dwInstance

Application-defined value specified in <a href="https://msdn.microsoft.com/3e93284d-2810-4c8e-9619-1989d8bf788e">acmDriverEnum</a>.


### -param fdwSupport

Driver-support flags specific to the driver specified by <i>hadid</i>. These flags are identical to the <b>fdwSupport</b> flags of the <a href="https://msdn.microsoft.com/b45b26e2-a9c0-4d01-9989-a071d9c73993">ACMDRIVERDETAILS</a> structure. This parameter can be a combination of the following values.

<table>
<tr>
<th>Value
</th>
<th>Meaning
</th>
</tr>
<tr>
<td>ACMDRIVERDETAILS_SUPPORTF_ASYNC</td>
<td>Driver supports asynchronous conversions.</td>
</tr>
<tr>
<td>ACMDRIVERDETAILS_SUPPORTF_CODEC</td>
<td>Driver supports conversion between two different format tags. For example, if a driver supports compression from WAVE_FORMAT_PCM to WAVE_FORMAT_ADPCM, this flag is set.</td>
</tr>
<tr>
<td>ACMDRIVERDETAILS_SUPPORTF_CONVERTER</td>
<td>Driver supports conversion between two different formats of the same format tag. For example, if a driver supports resampling of WAVE_FORMAT_PCM, this flag is set.</td>
</tr>
<tr>
<td>ACMDRIVERDETAILS_SUPPORTF_DISABLED</td>
<td>Driver has been disabled. An application must specify the ACM_DRIVERENUMF_DISABLED flag with <a href="https://msdn.microsoft.com/3e93284d-2810-4c8e-9619-1989d8bf788e">acmDriverEnum</a> to include disabled drivers in the enumeration.</td>
</tr>
<tr>
<td>ACMDRIVERDETAILS_SUPPORTF_FILTER</td>
<td>Driver supports a filter (modification of the data without changing any of the format attributes). For example, if a driver supports volume or echo operations on WAVE_FORMAT_PCM, this flag is set.</td>
</tr>
</table>
 


## -returns



The callback function must return <b>TRUE</b> to continue enumeration or <b>FALSE</b> to stop enumeration.




## -remarks



The <a href="https://msdn.microsoft.com/3e93284d-2810-4c8e-9619-1989d8bf788e">acmDriverEnum</a> function will return MMSYSERR_NOERROR (zero) if no ACM drivers are installed. Moreover, the callback function will not be called.

The following functions should not be called from within the callback function: <a href="https://msdn.microsoft.com/f037cab8-a1f4-487f-ab0a-11e11993b007">acmDriverAdd</a>, <a href="https://msdn.microsoft.com/7182d452-a935-4ed5-808a-595fca4f0429">acmDriverRemove</a>, and <a href="https://msdn.microsoft.com/62ab009e-b8fe-4b92-ba0f-a98cd761307b">acmDriverPriority</a>.




## -see-also




<a href="https://msdn.microsoft.com/da207a50-9c67-4cf3-920b-5878637060db">Audio Compression Functions</a>



<a href="https://msdn.microsoft.com/2f9a4540-86c0-40e6-b4da-24a9d31b56bf">Audio Compression Manager</a>
 

 

