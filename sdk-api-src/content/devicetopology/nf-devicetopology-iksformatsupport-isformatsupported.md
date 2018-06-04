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

# IKsFormatSupport::IsFormatSupported


## -description



The <b>IsFormatSupported</b> method indicates whether the audio endpoint device supports the specified audio stream format.




## -parameters




### -param pKsFormat [in]

Pointer to an audio-stream format specifier. This parameter points to a caller-allocated buffer that contains a format specifier. The specifier begins with a <a href="https://msdn.microsoft.com/library/windows/hardware/ff561656">KSDATAFORMAT</a> structure that might be followed by additional format information. For more information about <b>KSDATAFORMAT</b> and format specifiers, see the Windows DDK documentation.


### -param cbFormat [in]

The size in bytes of the buffer that contains the format specifier.


### -param pbSupported [out]

Pointer to a <b>BOOL</b> variable into which the method writes a value to indicate whether the format is supported. The method writes <b>TRUE</b> if the device supports the format and <b>FALSE</b> if the device does not support the format.


## -returns



If the method succeeds, it returns S_OK. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

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
Pointer <i>pKsFormat</i> or <i>pbSupported</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The format specifier is not valid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/53a29b57-1650-4e4d-b9d2-95307063a733">IKsFormatSupport Interface</a>
 

 

