---
UID: NF:msacm.acmFilterChooseW
title: acmFilterChooseW function
author: windows-sdk-content
description: The acmFilterChoose function creates an ACM-defined dialog box that enables the user to select a waveform-audio filter.
old-location: multimedia\acmfilterchoose.htm
old-project: Multimedia
ms.assetid: 9d8f659f-46f7-4399-a538-24c887c0fbee
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: "_win32_acmFilterChoose, acmFilterChoose, acmFilterChoose function [Windows Multimedia], acmFilterChooseA, acmFilterChooseW, msacm/acmFilterChoose, msacm/acmFilterChooseA, msacm/acmFilterChooseW, multimedia.acmfilterchoose"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: msacm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: acmFilterChooseW (Unicode) and acmFilterChooseA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SSTP_CONFIG_PARAMS, *PSSTP_CONFIG_PARAMS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msacm32.dll
 - Ext-MS-Win-mm-msacm-l1-1-0.dll
api_name:
 - acmFilterChoose
 - acmFilterChooseA
 - acmFilterChooseW
product: Windows
targetos: Windows
req.lib: Msacm32.lib
req.dll: Msacm32.dll
req.irql: 
req.product: GDI+ 1.1
---

# acmFilterChooseW function


## -description



The <b>acmFilterChoose</b> function creates an ACM-defined dialog box that enables the user to select a waveform-audio filter.




## -parameters




### -param pafltrc

Pointer to an <a href="https://msdn.microsoft.com/92ec2a41-e853-4533-b831-43c9d52dc27f">ACMFILTERCHOOSE</a> structure that contains information used to initialize the dialog box. When <b>acmFilterChoose</b> returns, this structure contains information about the user's filter selection.

The <b>pwfltr</b> member of this structure must contain a valid pointer to a memory location that will contain the returned filter header structure. The <b>cbwfltr</b> member must be filled in with the size, in bytes, of this memory buffer.


## -returns



Returns MMSYSERR_NOERROR if successful or an error otherwise. Possible error values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ACMERR_CANCELED</b></dt>
</dl>
</td>
<td width="60%">
The user chose the Cancel button or the Close command on the System menu to close the dialog box.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ACMERR_NOTPOSSIBLE</b></dt>
</dl>
</td>
<td width="60%">
The buffer identified by the <b>pwfltr</b> member of the <a href="https://msdn.microsoft.com/92ec2a41-e853-4533-b831-43c9d52dc27f">ACMFILTERCHOOSE</a> structure is too small to contain the selected filter.

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
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_NODRIVER</b></dt>
</dl>
</td>
<td width="60%">
A suitable driver is not available to provide valid filter selections.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/da207a50-9c67-4cf3-920b-5878637060db">Audio Compression Functions</a>



<a href="https://msdn.microsoft.com/2f9a4540-86c0-40e6-b4da-24a9d31b56bf">Audio Compression Manager</a>
 

 

