---
UID: NF:vss.IVssAsync.QueryStatus
title: IVssAsync::QueryStatus (vss.h)
description: The QueryStatus method queries the status of an asynchronous operation.
helpviewer_keywords: ["IVssAsync interface [VSS]","QueryStatus method","IVssAsync.QueryStatus","IVssAsync::QueryStatus","QueryStatus","QueryStatus method [VSS]","QueryStatus method [VSS]","IVssAsync interface","VSS_S_ASYNC_CANCELLED","VSS_S_ASYNC_FINISHED","VSS_S_ASYNC_PENDING","_win32_ivssasync_querystatus","base.ivssasync_querystatus","vss/IVssAsync::QueryStatus"]
old-location: base\ivssasync_querystatus.htm
tech.root: base
ms.assetid: 85fb3ae8-dc09-4f6f-a96b-e4dc046ff48a
ms.date: 12/05/2018
ms.keywords: IVssAsync interface [VSS],QueryStatus method, IVssAsync.QueryStatus, IVssAsync::QueryStatus, QueryStatus, QueryStatus method [VSS], QueryStatus method [VSS],IVssAsync interface, VSS_S_ASYNC_CANCELLED, VSS_S_ASYNC_FINISHED, VSS_S_ASYNC_PENDING, _win32_ivssasync_querystatus, base.ivssasync_querystatus, vss/IVssAsync::QueryStatus
req.header: vss.h
req.include-header: 
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
req.lib: VssApi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssAsync::QueryStatus
 - vss/IVssAsync::QueryStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssAsync.QueryStatus
---

# IVssAsync::QueryStatus


## -description

The <b>QueryStatus</b> method queries the status of an 
    asynchronous operation.

## -parameters

### -param pHrResult [out]

The status of the asynchronous operation that returned the current 
      <a href="/windows/desktop/api/vss/nn-vss-ivssasync">IVssAsync</a> object. 
      

All calls to <b>QueryStatus</b> for all 
       <a href="/windows/desktop/api/vss/nn-vss-ivssasync">IVssAsync</a> objects support the following status codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VSS_S_ASYNC_CANCELLED"></a><a id="vss_s_async_cancelled"></a><dl>
<dt><b>VSS_S_ASYNC_CANCELLED</b></dt>
</dl>
</td>
<td width="60%">
The asynchronous operation was canceled by a previous call to 
        <a href="/windows/desktop/api/vss/nf-vss-ivssasync-cancel">IVssAsync::Cancel</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="VSS_S_ASYNC_FINISHED"></a><a id="vss_s_async_finished"></a><dl>
<dt><b>VSS_S_ASYNC_FINISHED</b></dt>
</dl>
</td>
<td width="60%">
The asynchronous operation was completed successfully.

</td>
</tr>
<tr>
<td width="40%"><a id="VSS_S_ASYNC_PENDING"></a><a id="vss_s_async_pending"></a><dl>
<dt><b>VSS_S_ASYNC_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The asynchronous operation is still running.

</td>
</tr>
</table>
 

Additional return values can be returned, but depend on the return codes of the method that initially 
       returned the <a href="/windows/desktop/api/vss/nn-vss-ivssasync">IVssAsync</a> object.

### -param pReserved [out]

The value of this parameter should be <b>NULL</b>.

## -returns

The following are the valid return codes for this method.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The query operation was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The query operation failed because the user did not have the correct privileges.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The pointer to the variable used to hold the <i>pHrResult</i> return value is 
        <b>NULL</b> or is not a valid memory location.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected error. The error code is logged in the error log file. For more information, see 
        <a href="/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported until Windows Server 2008 R2 and Windows 7. E_UNEXPECTED is used instead.

</td>
</tr>
</table>

## -remarks

In the event of an error during the course of an asynchronous operation, 
    <b>QueryStatus</b> will return the same error code as the 
    method that initially returned the <a href="/windows/desktop/api/vss/nn-vss-ivssasync">IVssAsync</a> object.

To obtain a complete list of return values for an 
    <b>IVssAsync::QueryStatus</b> object returned by a 
    specific method, see the error codes documented for that method.

## -see-also

<a href="/windows/desktop/api/vss/nn-vss-ivssasync">IVssAsync</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset">IVssBackupComponents::DoSnapshotSet</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata">IVssBackupComponents::GatherWriterMetadata</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus">IVssBackupComponents::GatherWriterStatus</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-importsnapshots">IVssBackupComponents::ImportSnapshots</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-postrestore">IVssBackupComponents::PostRestore</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-prerestore">IVssBackupComponents::PreRestore</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup">IVssBackupComponents::PrepareForBackup</a>