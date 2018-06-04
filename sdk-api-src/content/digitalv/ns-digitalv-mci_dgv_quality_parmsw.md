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

# MCI_DGV_QUALITY_PARMSW structure


## -description



The <b>MCI_DGV_QUALITY_PARMS</b> structure contains parameters for the <a href="https://msdn.microsoft.com/91ad9704-0089-4b1f-b0f6-919ab5fd84e0">MCI_QUALITY</a> command for digital-video devices.




## -struct-fields




### -field dwCallback

The low-order word specifies a window handle used for the MCI_NOTIFY flag.


### -field dwItem

One of the following constants indicating the type of algorithm:

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="MCI_QUALITY_ITEM_AUDIO"></a><a id="mci_quality_item_audio"></a><dl>
<dt><b>MCI_QUALITY_ITEM_AUDIO</b></dt>
</dl>
</td>
<td width="60%">
Definitions are for an audio compression algorithm.

</td>
</tr>
<tr>
<td width="40%"><a id="MCI_QUALITY_ITEM_STILL"></a><a id="mci_quality_item_still"></a><dl>
<dt><b>MCI_QUALITY_ITEM_STILL</b></dt>
</dl>
</td>
<td width="60%">
Definitions are for a still video compression algorithm.

</td>
</tr>
<tr>
<td width="40%"><a id="MCI_QUALITY_ITEM_VIDEO"></a><a id="mci_quality_item_video"></a><dl>
<dt><b>MCI_QUALITY_ITEM_VIDEO</b></dt>
</dl>
</td>
<td width="60%">
Definitions are for a video compression algorithm.

</td>
</tr>
</table>
 


### -field lpstrName

String naming description.


### -field lpstrAlgorithm

String naming algorithm.


### -field dwHandle

Handle to a structure containing information describing the quality attributes.


## -remarks



When assigning data to the members of this structure, set the corresponding flags in the <i>fdwCommand</i> parameter of the <a href="https://msdn.microsoft.com/e25820e9-2caf-423e-8588-f842e670e0c3">mciSendCommand</a> function to validate the members.




## -see-also




<a href="https://msdn.microsoft.com/b414dffb-3701-4dfd-aa8c-cd8e8918027d">MCI</a>



<a href="https://msdn.microsoft.com/e86740e5-633e-465d-94ef-8065a8c05b31">MCI Structures</a>



<a href="https://msdn.microsoft.com/91ad9704-0089-4b1f-b0f6-919ab5fd84e0">MCI_QUALITY</a>



<a href="https://msdn.microsoft.com/e25820e9-2caf-423e-8588-f842e670e0c3">mciSendCommand</a>
 

 

