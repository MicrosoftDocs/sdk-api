---
UID: NS:winioctl.DELETE_USN_JOURNAL_DATA
title: DELETE_USN_JOURNAL_DATA
description: Contains information on the deletion of an update sequence number (USN) change journal using the FSCTL_DELETE_USN_JOURNAL control code.
helpviewer_keywords: ["*PDELETE_USN_JOURNAL_DATA","DELETE_USN_JOURNAL_DATA","DELETE_USN_JOURNAL_DATA structure [Files]","PDELETE_USN_JOURNAL_DATA","PDELETE_USN_JOURNAL_DATA structure pointer [Files]","USN_DELETE_FLAG_DELETE","USN_DELETE_FLAG_NOTIFY","_win32_delete_usn_journal_data_str","base.delete_usn_journal_data_str","fs.delete_usn_journal_data_str","winioctl/DELETE_USN_JOURNAL_DATA","winioctl/PDELETE_USN_JOURNAL_DATA"]
old-location: fs\delete_usn_journal_data_str.htm
tech.root: fs
ms.assetid: 06db4b46-fc91-40e0-ab0b-1e014622ae22
ms.date: 12/05/2018
ms.keywords: '*PDELETE_USN_JOURNAL_DATA, DELETE_USN_JOURNAL_DATA, DELETE_USN_JOURNAL_DATA structure [Files], PDELETE_USN_JOURNAL_DATA, PDELETE_USN_JOURNAL_DATA structure pointer [Files], USN_DELETE_FLAG_DELETE, USN_DELETE_FLAG_NOTIFY, _win32_delete_usn_journal_data_str, base.delete_usn_journal_data_str, fs.delete_usn_journal_data_str, winioctl/DELETE_USN_JOURNAL_DATA, winioctl/PDELETE_USN_JOURNAL_DATA'
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: DELETE_USN_JOURNAL_DATA, *PDELETE_USN_JOURNAL_DATA
req.redist: 
f1_keywords:
 - PDELETE_USN_JOURNAL_DATA
 - winioctl/PDELETE_USN_JOURNAL_DATA
 - DELETE_USN_JOURNAL_DATA
 - winioctl/DELETE_USN_JOURNAL_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - DELETE_USN_JOURNAL_DATA
---

# DELETE_USN_JOURNAL_DATA structure


## -description

Contains information on the deletion of an update sequence number (USN) change journal using the 
<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_delete_usn_journal">FSCTL_DELETE_USN_JOURNAL</a> control code.

## -struct-fields

### -field UsnJournalID

The identifier of the change journal to be deleted. 




If the journal is active and deletion is requested by setting the USN_DELETE_FLAG_DELETE flag in the <b>DeleteFlags</b> member, then this identifier must specify the change journal for the current volume. Use 
<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_query_usn_journal">FSCTL_QUERY_USN_JOURNAL</a> to retrieve the identifier of this change journal. If in this case the identifier is not for the current volume's change journal, 
<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_delete_usn_journal">FSCTL_DELETE_USN_JOURNAL</a> fails.

If notification instead of deletion is requested by setting only the USN_DELETE_FLAG_NOTIFY flag in <b>DeleteFlags</b>, <b>UsnJournalID</b> is ignored.

### -field DeleteFlags

Indicates whether deletion or notification regarding deletion is performed, or both. The <b>DeleteFlags</b> member must contain one or both of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="USN_DELETE_FLAG_DELETE"></a><a id="usn_delete_flag_delete"></a><dl>
<dt><b>USN_DELETE_FLAG_DELETE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
If this flag is set and the USN_DELETE_FLAG_NOTIFY flag is not set, the 
<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_delete_usn_journal">FSCTL_DELETE_USN_JOURNAL</a> operation starts the journal deletion process and returns immediately. The journal deletion process continues, if necessary, across system restarts.


If this flag is set and the USN_DELETE_FLAG_NOTIFY flag is also set, both deletion and notification occur.
If this flag is set and the journal is active, you must provide the identifier for the change journal for the current volume in <b>UsnJournalID</b> or the operation fails. If the journal is not active, then <b>UsnJournalID</b> is ignored and the journal is deleted.

</td>
</tr>
<tr>
<td width="40%"><a id="USN_DELETE_FLAG_NOTIFY"></a><a id="usn_delete_flag_notify"></a><dl>
<dt><b>USN_DELETE_FLAG_NOTIFY</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the call sets up notification about when deletion is complete. The journal deletion request is completed when the journal deletion process is complete. If this flag is set and the USN_DELETE_FLAG_DELETE flag is not set, then the call sets up notification of a deletion that may already be in progress. For example, when your application starts, it might use this flag to determine if a deletion is in progress.


If this flag is set and the USN_DELETE_FLAG_DELETE flag is also set, both deletion and notification occur.
The notification is performed using an I/O completion port or another mechanism for asynchronous event notification.

</td>
</tr>
</table>

## -remarks

For more information, see 
<a href="/windows/desktop/FileIO/creating-modifying-and-deleting-a-change-journal">Creating, Modifying, and Deleting a Change Journal</a>.

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_delete_usn_journal">FSCTL_DELETE_USN_JOURNAL</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_query_usn_journal">FSCTL_QUERY_USN_JOURNAL</a>

