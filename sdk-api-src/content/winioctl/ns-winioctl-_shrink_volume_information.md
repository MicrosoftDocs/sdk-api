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

# _SHRINK_VOLUME_INFORMATION structure


## -description


Specifies the volume shrink operation to perform.


## -struct-fields




### -field ShrinkRequestType

Indicates the operation to perform. The valid values are as follows. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ShrinkPrepare"></a><a id="shrinkprepare"></a><a id="SHRINKPREPARE"></a><dl>
<dt><b>ShrinkPrepare</b></dt>
</dl>
</td>
<td width="60%">
Volume should perform any steps necessary to prepare for a shrink operation.

</td>
</tr>
<tr>
<td width="40%"><a id="ShrinkCommit"></a><a id="shrinkcommit"></a><a id="SHRINKCOMMIT"></a><dl>
<dt><b>ShrinkCommit</b></dt>
</dl>
</td>
<td width="60%">
Volume should commit the shrink operation changes.

</td>
</tr>
<tr>
<td width="40%"><a id="ShrinkAbort"></a><a id="shrinkabort"></a><a id="SHRINKABORT"></a><dl>
<dt><b>ShrinkAbort</b></dt>
</dl>
</td>
<td width="60%">
Volume should terminate the shrink operation.

</td>
</tr>
</table>
 


### -field Flags

This member must be zero.


### -field NewNumberOfSectors

The number of sectors that should be in the shrunken volume. Used only when the <b>ShrinkRequestType</b> member is <b>ShrinkPrepare</b>, otherwise this member should be initialized to zero.


## -see-also




<a href="https://msdn.microsoft.com/cf545417-f933-4054-bed4-e6adbf822f9c">FSCTL_SHRINK_VOLUME</a>
 

 

