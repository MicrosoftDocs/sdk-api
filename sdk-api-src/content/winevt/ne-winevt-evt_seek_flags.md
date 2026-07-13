---
UID: NE:winevt._EVT_SEEK_FLAGS
title: EVT_SEEK_FLAGS (winevt.h)
description: Defines the relative position in the result set from which to seek.
helpviewer_keywords: ["EVT_SEEK_FLAGS","EVT_SEEK_FLAGS enumeration [EventLog]","EvtSeekOriginMask","EvtSeekRelativeToBookmark","EvtSeekRelativeToCurrent","EvtSeekRelativeToFirst","EvtSeekRelativeToLast","EvtSeekStrict","wes.evt_seek_flags","winevt/EVT_SEEK_FLAGS","winevt/EvtSeekOriginMask","winevt/EvtSeekRelativeToBookmark","winevt/EvtSeekRelativeToCurrent","winevt/EvtSeekRelativeToFirst","winevt/EvtSeekRelativeToLast","winevt/EvtSeekStrict"]
old-location: wes\evt_seek_flags.htm
tech.root: wes
ms.assetid: 5340815b-b94a-488b-bfa1-01dcbc15e505
ms.date: 12/05/2018
ms.keywords: EVT_SEEK_FLAGS, EVT_SEEK_FLAGS enumeration [EventLog], EvtSeekOriginMask, EvtSeekRelativeToBookmark, EvtSeekRelativeToCurrent, EvtSeekRelativeToFirst, EvtSeekRelativeToLast, EvtSeekStrict, wes.evt_seek_flags, winevt/EVT_SEEK_FLAGS, winevt/EvtSeekOriginMask, winevt/EvtSeekRelativeToBookmark, winevt/EvtSeekRelativeToCurrent, winevt/EvtSeekRelativeToFirst, winevt/EvtSeekRelativeToLast, winevt/EvtSeekStrict
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
targetos: Windows
req.typenames: EVT_SEEK_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EVT_SEEK_FLAGS
 - winevt/_EVT_SEEK_FLAGS
 - EVT_SEEK_FLAGS
 - winevt/EVT_SEEK_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinEvt.h
api_name:
 - EVT_SEEK_FLAGS
---

# EVT_SEEK_FLAGS enumeration


## -description

Defines the relative position in the result set from which to seek.

## -enum-fields

### -field EvtSeekRelativeToFirst:1

Seek to the specified offset from the first entry in the result set. The offset must be a positive value.

### -field EvtSeekRelativeToLast:2

Seek to the specified offset from the last entry in the result set. The offset must be a negative value.

### -field EvtSeekRelativeToCurrent:3

Seek to the specified offset from the current entry in the result set. The offset can be a positive or negative value.

### -field EvtSeekRelativeToBookmark:4

Seek to the specified offset from the bookmarked entry in the result set. The offset can be a positive or negative value.

### -field EvtSeekOriginMask:7

A bitmask that you can use to determine which of the following flags is set:

<ul>
<li>EvtSeekRelativeToFirst</li>
<li>EvtSeekRelativeToLast</li>
<li>EvtSeekRelativeToBookmark</li>
</ul>

### -field EvtSeekStrict:0x10000

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

<a href="/windows/desktop/api/winevt/nf-winevt-evtseek">EvtSeek</a>
