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

# IBDA_DRIDRMService::GetPairingStatus


## -description



      The <b>GetPairingStatus</b> method gets the Digital Rights Management (DRM) pairing status for a Media Transform Device (MTD) in a graph under the Protected Broadcast Driver Architecture (PBDA). This status indicates whether a secure pairing exists between the MTD and a Media Sink Device (MSD) so that controlled-access (CA) content can be released.


## -parameters




### -param penumPairingStatus [in, out]


            Address of a variable that gets the pairing device status. The caller passes in a pointer to this variable, and this method returns the correct status value in this parameter. The pairing status that is passed back  can be any of the following values:
          

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="_Green_"></a><a id="_green_"></a><a id="_GREEN_"></a><dl>
<dt><b>"Green"</b></dt>
</dl>
</td>
<td width="60%">
The MTD is paired with an MSD, so CA content is released under DRM protection.

</td>
</tr>
<tr>
<td width="40%"><a id="_Orange_"></a><a id="_orange_"></a><a id="_ORANGE_"></a><dl>
<dt><b>"Orange"</b></dt>
</dl>
</td>
<td width="60%">
The MTD is paired with an MSD, but this pairing is about to time out. The MSD is expected to refresh its pairing in the background. CA content is released under DRM protection.

</td>
</tr>
<tr>
<td width="40%"><a id="_Red_"></a><a id="_red_"></a><a id="_RED_"></a><dl>
<dt><b>"Red"</b></dt>
</dl>
</td>
<td width="60%">
The MTD is not paired with an MSD, so CA content is is not released.

</td>
</tr>
</table>
 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/9b04c960-a766-4322-bf18-e59176ee2ad1">IBDA_DRIDRMService</a>
 

 

