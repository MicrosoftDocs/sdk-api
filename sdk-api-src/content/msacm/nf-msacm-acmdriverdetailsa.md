---
UID: NF:msacm.acmDriverDetailsA
title: acmDriverDetailsA function (msacm.h)
description: The acmDriverDetails function queries a specified ACM driver to determine its capabilities.
helpviewer_keywords: ["_win32_acmDriverDetails","acmDriverDetails","acmDriverDetails function [Windows Multimedia]","acmDriverDetailsA","acmDriverDetailsW","msacm/acmDriverDetails","msacm/acmDriverDetailsA","msacm/acmDriverDetailsW","multimedia.acmdriverdetails"]
old-location: multimedia\acmdriverdetails.htm
tech.root: Multimedia
ms.assetid: f8fcce73-1cac-463d-8e2d-1372d6b64614
ms.date: 12/05/2018
ms.keywords: _win32_acmDriverDetails, acmDriverDetails, acmDriverDetails function [Windows Multimedia], acmDriverDetailsA, acmDriverDetailsW, msacm/acmDriverDetails, msacm/acmDriverDetailsA, msacm/acmDriverDetailsW, multimedia.acmdriverdetails
f1_keywords:
- msacm/acmDriverDetails
dev_langs:
- c++
req.header: msacm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: acmDriverDetailsW (Unicode) and acmDriverDetailsA (ANSI)
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
- acmDriverDetails
- acmDriverDetailsA
- acmDriverDetailsW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# acmDriverDetailsA function


## -description



The <b>acmDriverDetails</b> function queries a specified ACM driver to determine its capabilities.




## -parameters




### -param hadid

Handle to the driver identifier of an installed ACM driver. Disabled drivers can be queried for details.


### -param padd

Pointer to an [ACMDRIVERDETAILS](/windows/win32/api/msacm/nf-msacm-acmdriverdetails) structure that will receive the driver details. The <b>cbStruct</b> member must be initialized to the size, in bytes, of the structure.


### -param fdwDetails

Reserved; must be zero.


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
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/audio-compression-functions">Audio Compression Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/audio-compression-manager">Audio Compression Manager</a>
 

 

