---
UID: NF:vss.IVssAsync.QueryStatus
title: IVssAsync::QueryStatus
author: windows-sdk-content
description: The QueryStatus method queries the status of an asynchronous operation.
old-location: base\ivssasync_querystatus.htm
old-project: vss
ms.assetid: 85fb3ae8-dc09-4f6f-a96b-e4dc046ff48a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IVssAsync interface [VSS],QueryStatus method, IVssAsync.QueryStatus, IVssAsync::QueryStatus, QueryStatus, QueryStatus method [VSS], QueryStatus method [VSS],IVssAsync interface, VSS_S_ASYNC_CANCELLED, VSS_S_ASYNC_FINISHED, VSS_S_ASYNC_PENDING, _win32_ivssasync_querystatus, base.ivssasync_querystatus, vss/IVssAsync::QueryStatus
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: VSS_WRITER_STATE, *PVSS_WRITER_STATE
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
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssAsync::QueryStatus


## -description


The <b>QueryStatus</b> method queries the status of an 
    asynchronous operation.


## -parameters




### -param pHrResult [out]

The status of the asynchronous operation that returned the current 
      <a href="https://msdn.microsoft.com/d2cff547-b4ff-454d-8e0e-cd29b91cbb07">IVssAsync</a> object. 
      

All calls to <b>QueryStatus</b> for all 
       <a href="https://msdn.microsoft.com/d2cff547-b4ff-454d-8e0e-cd29b91cbb07">IVssAsync</a> objects support the following status codes.

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
        <a href="https://msdn.microsoft.com/8ab44737-114b-4edc-a097-d0fa297f6276">IVssAsync::Cancel</a>.

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
       returned the <a href="https://msdn.microsoft.com/d2cff547-b4ff-454d-8e0e-cd29b91cbb07">IVssAsync</a> object.


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
        <a href="https://msdn.microsoft.com/6377d937-5739-45f5-9195-5d18be4069ce">Event and Error Handling Under VSS</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported until Windows Server 2008 R2 and Windows 7. E_UNEXPECTED is used instead.

</td>
</tr>
</table>
 




## -remarks



In the event of an error during the course of an asynchronous operation, 
    <b>QueryStatus</b> will return the same error code as the 
    method that initially returned the <a href="https://msdn.microsoft.com/d2cff547-b4ff-454d-8e0e-cd29b91cbb07">IVssAsync</a> object.

To obtain a complete list of return values for an 
    <b>IVssAsync::QueryStatus</b> object returned by a 
    specific method, see the error codes documented for that method.




## -see-also




<a href="https://msdn.microsoft.com/d2cff547-b4ff-454d-8e0e-cd29b91cbb07">IVssAsync</a>



<a href="https://msdn.microsoft.com/3cc6c375-8a24-4af3-b4ad-5a695cc2645c">IVssBackupComponents::DoSnapshotSet</a>



<a href="https://msdn.microsoft.com/44f19c10-c966-4ab6-98dd-865d535955db">IVssBackupComponents::GatherWriterMetadata</a>



<a href="https://msdn.microsoft.com/ca87cdc3-e233-4efc-81c0-918e5a698af5">IVssBackupComponents::GatherWriterStatus</a>



<a href="https://msdn.microsoft.com/7f28c841-5448-4ed7-b76e-0aa5376fd8bf">IVssBackupComponents::ImportSnapshots</a>



<a href="https://msdn.microsoft.com/01cf3931-59ef-4572-9f2e-aa210da0ac2d">IVssBackupComponents::PostRestore</a>



<a href="https://msdn.microsoft.com/7a4c8869-9655-49a7-818b-98a08103f4b4">IVssBackupComponents::PreRestore</a>



<a href="https://msdn.microsoft.com/46ce8282-a434-4b0b-b66e-40810052b34b">IVssBackupComponents::PrepareForBackup</a>
 

 

