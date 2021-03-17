---
UID: NS:clfsmgmt._CLFS_MGMT_NOTIFICATION
title: CLFS_MGMT_NOTIFICATION (clfsmgmt.h)
description: The CLFS_MGMT_NOTIFICATION structure specifies information about the notifications that the client receives.
helpviewer_keywords: ["*PCLFS_MGMT_NOTIFICATION","CLFS_MGMT_NOTIFICATION","CLFS_MGMT_NOTIFICATION structure [Files]","ClfsMgmtAdvanceTailNotification","ClfsMgmtLogFullHandlerNotification","ClfsMgmtLogUnpinnedNotification","ClfsMgmtLogWriteNotification","PCLFS_MGMT_NOTIFICATION","PCLFS_MGMT_NOTIFICATION structure pointer [Files]","clfsmgmt/CLFS_MGMT_NOTIFICATION","clfsmgmt/PCLFS_MGMT_NOTIFICATION","fs.clfs_mgmt_notification"]
old-location: fs\clfs_mgmt_notification.htm
tech.root: fs
ms.assetid: ba7f7414-885f-40d0-ab61-2348d7f6125b
ms.date: 12/05/2018
ms.keywords: '*PCLFS_MGMT_NOTIFICATION, CLFS_MGMT_NOTIFICATION, CLFS_MGMT_NOTIFICATION structure [Files], ClfsMgmtAdvanceTailNotification, ClfsMgmtLogFullHandlerNotification, ClfsMgmtLogUnpinnedNotification, ClfsMgmtLogWriteNotification, PCLFS_MGMT_NOTIFICATION, PCLFS_MGMT_NOTIFICATION structure pointer [Files], clfsmgmt/CLFS_MGMT_NOTIFICATION, clfsmgmt/PCLFS_MGMT_NOTIFICATION, fs.clfs_mgmt_notification'
req.header: clfsmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
req.typenames: CLFS_MGMT_NOTIFICATION, *PCLFS_MGMT_NOTIFICATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CLFS_MGMT_NOTIFICATION
 - clfsmgmt/_CLFS_MGMT_NOTIFICATION
 - PCLFS_MGMT_NOTIFICATION
 - clfsmgmt/PCLFS_MGMT_NOTIFICATION
 - CLFS_MGMT_NOTIFICATION
 - clfsmgmt/CLFS_MGMT_NOTIFICATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClfsMgmt.h
api_name:
 - CLFS_MGMT_NOTIFICATION
---

# CLFS_MGMT_NOTIFICATION structure


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
        <a href="/windows/desktop/api/clfsmgmtw32/nc-clfsmgmtw32-plog_tail_advance_callback">LOG_TAIL_ADVANCE_CALLBACK</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="ClfsMgmtLogFullHandlerNotification"></a><a id="clfsmgmtlogfullhandlernotification"></a><a id="CLFSMGMTLOGFULLHANDLERNOTIFICATION"></a><dl>
<dt><b>ClfsMgmtLogFullHandlerNotification</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The notification that a  call to <a href="/windows/desktop/api/clfsmgmtw32/nf-clfsmgmtw32-handlelogfull">HandleLogFull</a> is 
        complete. For more information, see 
        <a href="/windows/desktop/api/clfsmgmtw32/nc-clfsmgmtw32-plog_full_handler_callback">LOG_FULL_HANDLER_CALLBACK</a>.

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
        <a href="/windows/desktop/api/clfsmgmtw32/nc-clfsmgmtw32-plog_unpinned_callback">LOG_UNPINNED_CALLBACK</a>.

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
        <a href="/windows/desktop/api/clfsmgmtw32/nf-clfsmgmtw32-registerforlogwritenotification">RegisterForLogWriteNotification</a>.
        

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

<a href="/previous-versions/windows/desktop/clfs/clfs-management-structures">CLFS Management Structures</a>



<a href="/windows/desktop/api/clfsmgmtw32/nf-clfsmgmtw32-readlognotification">ReadLogNotification</a>