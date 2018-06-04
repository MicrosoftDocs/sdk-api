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

# IMFASFStreamSelector::GetBandwidthStep


## -description



Retrieves the stream numbers that apply to a bandwidth step. This method is used for multiple bit rate (MBR) content.




## -parameters




### -param dwStepNum [in]

Bandwidth step number for which to retrieve information. Set this value to a number between 0, and 1 less than the number of bandwidth steps returned by <a href="https://msdn.microsoft.com/6b7105c1-7395-462f-ad52-daf621258714">IMFASFStreamSelector::GetBandwidthStepCount</a>.


### -param pdwBitrate [out]

Receives the bit rate associated with the bandwidth step.


### -param rgwStreamNumbers [out]

Address of an array that receives the stream numbers. The caller allocates the array. The array size must be at least as large as the value returned by the <a href="https://msdn.microsoft.com/e1e80c32-bfd4-4404-9ccc-05b5077b83a6">IMFASFStreamSelector::GetStreamCount</a> method.



### -param rgSelections [out]

Address of an array that receives the selection status of each stream, as an <a href="https://msdn.microsoft.com/1571650b-4d5c-49ae-9e6d-77ef4ae7ae59">ASF_SELECTION_STATUS</a> value. The members of this array correspond to the members of the <i>rgwStreamNumbers</i> array by index. The caller allocates the array. The array size must be at least as large as the value returned by the <a href="https://msdn.microsoft.com/e1e80c32-bfd4-4404-9ccc-05b5077b83a6">IMFASFStreamSelector::GetStreamCount</a> method.



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



Bandwidth steps are bandwidth levels used for MBR content. If you stream MBR content, you can choose the bandwidth step that matches the network conditions to avoid interruptions during playback.




## -see-also




<a href="https://msdn.microsoft.com/d2e1fc15-2e12-4698-a4b1-ca8046d228de">IMFASFStreamSelector</a>



<a href="https://msdn.microsoft.com/6b7105c1-7395-462f-ad52-daf621258714">IMFASFStreamSelector::GetBandwidthStepCount</a>
 

 

