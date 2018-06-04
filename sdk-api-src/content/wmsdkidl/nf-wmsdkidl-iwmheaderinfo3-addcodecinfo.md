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

# IWMHeaderInfo3::AddCodecInfo


## -description



The <b>AddCodecInfo</b> method adds codec information to a file. When you copy a compressed stream from one file to another, use this method to include the information about the encoding codec in the file header.




## -parameters




### -param pwszName [in]

Pointer to a wide-character null-terminated string containing the name.


### -param pwszDescription [in]

Pointer to a wide-character null-terminated string containing the description.


### -param codecType [in]

A value from the <a href="https://msdn.microsoft.com/31fcaa84-1b7e-407c-95dc-bf13263b788a">WMT_CODEC_INFO_TYPE</a> enumeration specifying the codec type.


### -param cbCodecInfo [in]

The size of the codec information, in bytes.


### -param pbCodecInfo [in]

Pointer to an array of bytes that contains the codec information.


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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



The parameters passed to this method should be obtained from the original file with a call to <a href="https://msdn.microsoft.com/685eaf9e-6cc8-4c38-be34-afa4b504a326">IWMHeaderInfo2::GetCodecInfo</a>.




## -see-also




<a href="https://msdn.microsoft.com/5791e330-3877-4d3a-b27f-f14b97d1a435">IWMHeaderInfo3 Interface</a>
 

 

