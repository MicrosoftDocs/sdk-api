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

# IWMReaderTimecode::GetTimecodeRangeBounds


## -description



The <b>GetTimecodeRangeBounds</b> method retrieves the starting and ending time codes for a specified SMPTE time code range.




## -parameters




### -param wStreamNum [in]

<b>WORD</b> containing the stream number.


### -param wRangeNum [in]

<b>WORD</b> containing the range number.


### -param pStartTimecode [out]

Pointer to a <b>DWORD</b> containing the first time code in the range.


### -param pEndTimecode [out]

Pointer to a <b>DWORD</b> containing the last time code in the range.


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
 




## -see-also




<a href="https://msdn.microsoft.com/7f7d5608-c505-46ab-9e1e-e45b383c879b">IWMReaderTimecode Interface</a>



<a href="https://msdn.microsoft.com/df58f968-23f8-407b-b18c-569732635464">IWMReaderTimecode::GetTimecodeRangeCount</a>
 

 

