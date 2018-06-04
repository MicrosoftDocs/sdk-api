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

# IWMPSettings::get_baseURL


## -description



The <b>get_baseURL</b> method retrieves the base URL used for relative path resolution with URL script commands that are embedded in digital media content.




## -parameters




### -param pbstrBaseURL [out]

Pointer to a <b>BSTR</b> containing the base URL.


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



This method retrieves the base HTTP URL that is passed as the command parameter by the <b>ScriptCommand</b> event. The base URL is concatenated with the relative URL as follows:

<ol>
<li>A trailing forward slash (/) is added to the value retrieved by the <b>get_baseURL</b> method.</li>
<li>A leading period, backward slash, or forward slash character (., \, and /) is deleted from the relative URL.</li>
<li>The relative URL is added to the end of the base URL.</li>
<li>All slash characters in the resulting fully qualified URL are pointed in the same direction (converted to forward or backward slashes) based on the direction of the first slash character encountered in the new URL.</li>
</ol>
<b>Note</b>

The Windows Media Player control does not support the use of two periods (..) in the relative URL to indicate the parent of the current location.

<b>Windows Media Player 10 Mobile: </b>This method always retrieves a <b>BSTR</b> containing an empty string.




## -see-also




<a href="https://msdn.microsoft.com/1010961f-6d06-455a-9c14-bc06702e9e89">IWMPEvents::ScriptCommand</a>



<a href="https://msdn.microsoft.com/e5a305a1-958e-4b6d-bb1f-f00bf5eb08dd">IWMPSettings Interface</a>



<a href="https://msdn.microsoft.com/ae070004-e90e-4f1e-b8b8-15deccdc48ad">IWMPSettings::put_baseURL</a>
 

 

