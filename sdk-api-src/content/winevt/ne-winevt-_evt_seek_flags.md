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

# _EVT_SEEK_FLAGS enumeration


## -description


Defines the relative position in the result set from which to seek.


## -enum-fields




### -field EvtSeekRelativeToFirst

Seek to the specified offset from the first entry in the result set. The offset must be a positive value.


### -field EvtSeekRelativeToLast

Seek to the specified offset from the last entry in the result set. The offset must be a negative value.


### -field EvtSeekRelativeToCurrent

Seek to the specified offset from the current entry in the result set. The offset can be a positive or negative value.


### -field EvtSeekRelativeToBookmark

Seek to the specified offset from the bookmarked entry in the result set. The offset can be a positive or negative value.


### -field EvtSeekOriginMask

A bitmask that you can use to determine which of the following flags is set:

<ul>
<li>EvtSeekRelativeToFirst</li>
<li>EvtSeekRelativeToLast</li>
<li>EvtSeekRelativeToBookmark</li>
</ul>

### -field EvtSeekStrict

Force the function to fail if the event does not exist.


## -remarks



If the offset or bookmark seeks past the boundary of the result set (past the first or last record), and EvtSeekStrict is not set, seek will return the last record within the boundary.

If the bookmark is within the boundaries of the result set (based on event record ID) but is not included in the result set, the seek function will apply the offset relative to the bookmark's record ID. In the following table, the first column shows the record IDs of the events in the result set. If the bookmark's record ID is 3989, the second column shows the record that the seek function would seek to given the specified offset.

<table>
<tr>
<th>Record ID</th>
<th>Offset</th>
</tr>
<tr>
<td>3995</td>
<td>–2</td>
</tr>
<tr>
<td>3991</td>
<td>–1</td>
</tr>
<tr>
<td>3987</td>
<td>0, 1</td>
</tr>
<tr>
<td>3983</td>
<td>2</td>
</tr>
<tr>
<td>3979</td>
<td>3</td>
</tr>
<tr>
<td>3975</td>
<td>4</td>
</tr>
<tr>
<td>3971</td>
<td>5</td>
</tr>
<tr>
<td>3968</td>
<td>6</td>
</tr>
<tr>
<td>3959</td>
<td>7</td>
</tr>
<tr>
<td>3955</td>
<td>8</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/62cf5039-f7c5-4f16-b7e3-dcc8907e6b7c">EvtSeek</a>
 

 

