---
UID: NE:winevt._EVT_SEEK_FLAGS
title: "_EVT_SEEK_FLAGS"
author: windows-sdk-content
description: Defines the relative position in the result set from which to seek.
old-location: wes\evt_seek_flags.htm
tech.root: WES
ms.assetid: 5340815b-b94a-488b-bfa1-01dcbc15e505
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: EVT_SEEK_FLAGS, EVT_SEEK_FLAGS enumeration [EventLog], EvtSeekOriginMask, EvtSeekRelativeToBookmark, EvtSeekRelativeToCurrent, EvtSeekRelativeToFirst, EvtSeekRelativeToLast, EvtSeekStrict, _EVT_SEEK_FLAGS, wes.evt_seek_flags, winevt/EVT_SEEK_FLAGS, winevt/EvtSeekOriginMask, winevt/EvtSeekRelativeToBookmark, winevt/EvtSeekRelativeToCurrent, winevt/EvtSeekRelativeToFirst, winevt/EvtSeekRelativeToLast, winevt/EvtSeekStrict
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: winevt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinEvt.h
api_name:
 - EVT_SEEK_FLAGS
product: Windows
targetos: Windows
req.typenames: EVT_SEEK_FLAGS
req.redist: 
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
 

 

