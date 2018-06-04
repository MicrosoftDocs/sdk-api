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

# IWMReaderTimecode::GetTimecodeRangeCount


## -description



The <b>GetTimecodeRangeCount</b> method retrieves the total number of SMTPE time code ranges in a specified stream.




## -parameters




### -param wStreamNum [in]

<b>WORD</b> containing the stream number. This stream must be indexed by time code.


### -param pwRangeCount [out]

Pointer to a <b>WORD</b> containing the number of ranges. If this parameter is 0 on method return, no SMPTE ranges exist in the stream.


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



<a href="https://msdn.microsoft.com/5bc1f21c-0aca-4e45-ac82-898cb8b9f4cc">IWMReaderTimecode::GetTimecodeRangeBounds</a>
 

 

