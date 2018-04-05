---
UID: NC:ntmsmli.CLAIMMEDIALABEL
title: CLAIMMEDIALABEL
author: windows-driver-content
description: The ClaimMediaLabel callback function determines whether a specified media label was created by the media's associated application.
old-location: fs\claimmedialabel.htm
old-project: Rsm
ms.assetid: ac957769-0513-436b-94f0-e3894f7a703b
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: ClaimMediaLabel, ClaimMediaLabel callback function [Files], _zaw_claimmedialabel, base.claimmedialabel, fs.claimmedialabel, ntmsmli/ClaimMediaLabel
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: ntmsmli.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: NTMS_STORAGESLOTINFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	NtmsMli.h
api_name:
-	ClaimMediaLabel
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# CLAIMMEDIALABEL callback


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/af7186f8-7921-48e3-a4fd-23259a6e9018">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<i>ClaimMediaLabel</i> callback function determines whether a specified media label was created by the media's associated application.


## -parameters




### -param pBuffer [in]

Pointer to a buffer that contains the media label.


### -param nBufferSize [in]

Size of the buffer, in bytes.


### -param pLabelInfo [out]

Pointer to a 
<a href="https://msdn.microsoft.com/8641e9e6-e251-4bf9-935a-f8888705f9a1">MediaLabelInfo</a> structure. The media label library fills in this structure if the library recognizes the media label.


## -returns



This function returns one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NO_ERROR</b></dt>
</dl>
</td>
<td width="60%">
The media label library filled in the 
<a href="https://msdn.microsoft.com/8641e9e6-e251-4bf9-935a-f8888705f9a1">MediaLabelInfo</a> structure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The media label library does not recognize the media label.

</td>
</tr>
</table>
 




## -remarks



When a media label library uses the 
<i>ClaimMediaLabel</i> function to identify the media label as one created by its associated application, the media label library must fill in the 
<a href="https://msdn.microsoft.com/8641e9e6-e251-4bf9-935a-f8888705f9a1">MediaLabelInfo</a> structure and return NO_ERROR. If the media label library does not recognize the media label, it returns ERROR_BAD_FORMAT.




## -see-also




<a href="removable_storage_manager_functions.htm">Media Label Library Functions</a>



<a href="https://msdn.microsoft.com/8641e9e6-e251-4bf9-935a-f8888705f9a1">MediaLabelInfo</a>
 

 

