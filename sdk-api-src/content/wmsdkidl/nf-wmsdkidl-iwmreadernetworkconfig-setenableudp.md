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

# IWMReaderNetworkConfig::SetEnableUDP


## -description



The <b>SetEnableUDP</b> method enables or disables UDP.




## -parameters




### -param fEnableUDP [in]

Boolean value that is True if UDP is to be enabled. Set this to true if the reader can use UDP-based MMS streaming when selecting a protocol for streaming.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
NULL or invalid argument passed in.

</td>
</tr>
</table>
 




## -remarks



This setting applies only to a protocol rollover or MMS://URL. Even if this setting is disabled, the application can still specify an explicit MMSU://URL and stream MMS via TCP successfully.

For more information, see the Remarks section of <a href="https://msdn.microsoft.com/10a11131-48bd-49bd-a767-1c6148f84b95">IWMReaderNetworkConfig::ResetProtocolRollover</a>.




## -see-also




<a href="https://msdn.microsoft.com/0957ece7-93fe-411b-b69e-fd03933b09d1">IWMReaderNetworkConfig Interface</a>



<a href="https://msdn.microsoft.com/6623c2f9-24cb-4038-9aa5-2eb634b3f1a2">IWMReaderNetworkConfig::GetEnableTCP</a>



<a href="https://msdn.microsoft.com/81c6536c-303c-4eac-a75a-54e9df29e299">IWMReaderNetworkConfig::GetEnableUDP</a>



<a href="https://msdn.microsoft.com/8afc62b8-a2f6-4470-8005-804e0980b599">IWMReaderNetworkConfig::SetEnableTCP</a>
 

 

