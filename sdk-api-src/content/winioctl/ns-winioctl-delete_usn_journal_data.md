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

# DELETE_USN_JOURNAL_DATA structure


## -description


Contains information on the deletion of an update sequence number (USN) change journal using the 
<a href="https://msdn.microsoft.com/6c85464d-019b-4923-9acf-152b4ee8c31b">FSCTL_DELETE_USN_JOURNAL</a> control code.


## -struct-fields




### -field UsnJournalID

The identifier of the change journal to be deleted. 




If the journal is active and deletion is requested by setting the USN_DELETE_FLAG_DELETE flag in the <b>DeleteFlags</b> member, then this identifier must specify the change journal for the current volume. Use 
<a href="https://msdn.microsoft.com/9491b054-934a-4b76-bf77-f397b6386f82">FSCTL_QUERY_USN_JOURNAL</a> to retrieve the identifier of this change journal. If in this case the identifier is not for the current volume's change journal, 
<a href="https://msdn.microsoft.com/6c85464d-019b-4923-9acf-152b4ee8c31b">FSCTL_DELETE_USN_JOURNAL</a> fails.

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
<a href="https://msdn.microsoft.com/6c85464d-019b-4923-9acf-152b4ee8c31b">FSCTL_DELETE_USN_JOURNAL</a> operation starts the journal deletion process and returns immediately. The journal deletion process continues, if necessary, across system restarts.


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
<a href="https://msdn.microsoft.com/26cbacc2-d26b-434b-91b5-31aedc96da13">Creating, Modifying, and Deleting a Change Journal</a>.




## -see-also




<a href="https://msdn.microsoft.com/6c85464d-019b-4923-9acf-152b4ee8c31b">FSCTL_DELETE_USN_JOURNAL</a>



<a href="https://msdn.microsoft.com/9491b054-934a-4b76-bf77-f397b6386f82">FSCTL_QUERY_USN_JOURNAL</a>
 

 

