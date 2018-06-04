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

# IWMWriterAdvanced3::GetStatisticsEx


## -description



The <b>GetStatisticsEx</b> method retrieves extended statistics for the writer.




## -parameters




### -param wStreamNum [in]

<b>WORD</b> containing the stream number for which you want to get statistics. You can pass 0 to obtain extended statistics for the entire file. Stream numbers are in the range of 1 through 63.


### -param pStats [out]

Pointer to the <a href="https://msdn.microsoft.com/f98a5934-968e-4c74-9fd2-f824ad77692c">WM_WRITER_STATISTICS_EX</a> structure that receives the statistics.


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
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
The writer is in the configuration state, during which this method cannot be called.

</td>
</tr>
</table>
 




## -remarks



<b>GetStatisticsEx</b> is not an improved version of <a href="https://msdn.microsoft.com/005c2039-e821-42ab-bead-1bf40f2ab171">IWMWriterAdvanced::GetStatistics</a>. The statistics retrieved by <b>GetStatistics</b> are not retrieved by <b>GetStatisticsEx</b>; if you want to get all available statistics you must call both methods.




## -see-also




<a href="https://msdn.microsoft.com/99f7e4f7-0080-498d-b4f1-960c4955b4db">IWMWriterAdvanced3 Interface</a>
 

 

