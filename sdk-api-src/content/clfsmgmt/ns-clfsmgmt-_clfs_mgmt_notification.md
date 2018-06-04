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

# _CLFS_MGMT_NOTIFICATION structure


## -description


The <b>CLFS_MGMT_NOTIFICATION</b> structure 
    specifies information about the notifications that the client receives.


## -struct-fields




### -field Notification


The type of notification to receive.  The following  values are valid.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ClfsMgmtAdvanceTailNotification"></a><a id="clfsmgmtadvancetailnotification"></a><a id="CLFSMGMTADVANCETAILNOTIFICATION"></a><dl>
<dt><b>ClfsMgmtAdvanceTailNotification</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
 The notification to advance the log tail. For more information, see 
        <a href="https://msdn.microsoft.com/dfa64e5e-55ef-4102-90d5-104b1a624267">LOG_TAIL_ADVANCE_CALLBACK</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="ClfsMgmtLogFullHandlerNotification"></a><a id="clfsmgmtlogfullhandlernotification"></a><a id="CLFSMGMTLOGFULLHANDLERNOTIFICATION"></a><dl>
<dt><b>ClfsMgmtLogFullHandlerNotification</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The notification that a  call to <a href="https://msdn.microsoft.com/ed4b067f-9386-4bec-a6dc-b22d6fd52390">HandleLogFull</a> is 
        complete. For more information, see 
        <a href="https://msdn.microsoft.com/7b8d3b94-2b2e-427e-9b89-530310ecc6fe">LOG_FULL_HANDLER_CALLBACK</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="ClfsMgmtLogUnpinnedNotification"></a><a id="clfsmgmtlogunpinnednotification"></a><a id="CLFSMGMTLOGUNPINNEDNOTIFICATION"></a><dl>
<dt><b>ClfsMgmtLogUnpinnedNotification</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The notification that the log is unpinned. For more information, see 
        <a href="https://msdn.microsoft.com/ab3b5ffb-01a5-4678-bcfa-7e71b1f4c0f3">LOG_UNPINNED_CALLBACK</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="ClfsMgmtLogWriteNotification"></a><a id="clfsmgmtlogwritenotification"></a><a id="CLFSMGMTLOGWRITENOTIFICATION"></a><dl>
<dt><b>ClfsMgmtLogWriteNotification</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The notification that a nonzero number of bytes has been written to the log. For more information, see 
        <a href="https://msdn.microsoft.com/08e197af-d88e-46dd-b862-66eb0ab27551">RegisterForLogWriteNotification</a>.
        

<b>Windows Server 2003 R2 and Windows Vista before SP1:  </b>This value is not supported.

</td>
</tr>
</table>
 


### -field Lsn

 If <b>Notification</b> is <b>ClfsMgmtAdvanceTailNotification</b>, 
      <b>Lsn</b> specifies the target log sequence number (LSN) the client should advance the log 
      tail to.


### -field LogIsPinned

If <b>Notification</b> is <b>ClfsMgmtLogUnpinnedNotification</b>, 
      <b>LogIsPinned</b> indicates  that the log is pinned. This member is 
      <b>TRUE</b> if the log is pinned.


## -see-also




<a href="https://msdn.microsoft.com/49304633-6f29-41ee-a3e1-06f884551de6">CLFS Management Structures</a>



<a href="https://msdn.microsoft.com/08931011-511b-471b-9a4a-ebc96e963c51">ReadLogNotification</a>
 

 

