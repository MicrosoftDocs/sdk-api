---
UID: NF:ddpbackup.IDedupBackupSupport.RestoreFiles
title: IDedupBackupSupport::RestoreFiles (ddpbackup.h)
description: Reconstructs a set of files from a backup store that contains the fully optimized version of the files (reparse points) and the Data Deduplication store.
helpviewer_keywords: ["DDP_E_FILE_CORRUPT","DDP_E_FILE_SYSTEM_CORRUPT","DDP_E_INVALID_DATA","DDP_E_JOB_COMPLETED_PARTIAL_SUCCESS","DDP_E_NOT_FOUND","DDP_E_PATH_NOT_FOUND","DDP_E_UNEXPECTED","DDP_E_VOLUME_DEDUP_DISABLED","DDP_E_VOLUME_UNSUPPORTED","IDedupBackupSupport interface [Data Deduplication API]","RestoreFiles method","IDedupBackupSupport.RestoreFiles","IDedupBackupSupport::RestoreFiles","RestoreFiles","RestoreFiles method [Data Deduplication API]","RestoreFiles method [Data Deduplication API]","IDedupBackupSupport interface","S_FALSE","S_OK","ddpbackup/IDedupBackupSupport::RestoreFiles","dedup.idedupbackupsupport_restorefile","dedup.idedupbackupsupport_restorefiles"]
old-location: dedup\idedupbackupsupport_restorefiles.htm
tech.root: dedup
ms.assetid: CFBB0B59-2869-4A30-8F2F-A473372B1E68
ms.date: 12/05/2018
ms.keywords: DDP_E_FILE_CORRUPT, DDP_E_FILE_SYSTEM_CORRUPT, DDP_E_INVALID_DATA, DDP_E_JOB_COMPLETED_PARTIAL_SUCCESS, DDP_E_NOT_FOUND, DDP_E_PATH_NOT_FOUND, DDP_E_UNEXPECTED, DDP_E_VOLUME_DEDUP_DISABLED, DDP_E_VOLUME_UNSUPPORTED, IDedupBackupSupport interface [Data Deduplication API],RestoreFiles method, IDedupBackupSupport.RestoreFiles, IDedupBackupSupport::RestoreFiles, RestoreFiles, RestoreFiles method [Data Deduplication API], RestoreFiles method [Data Deduplication API],IDedupBackupSupport interface, S_FALSE, S_OK, ddpbackup/IDedupBackupSupport::RestoreFiles, dedup.idedupbackupsupport_restorefile, dedup.idedupbackupsupport_restorefiles
req.header: ddpbackup.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DdpBackup.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDedupBackupSupport::RestoreFiles
 - ddpbackup/IDedupBackupSupport::RestoreFiles
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DdpBackup.h
api_name:
 - IDedupBackupSupport.RestoreFiles
---

# IDedupBackupSupport::RestoreFiles


## -description

Reconstructs a set of files from a backup store that contains the fully optimized version of the files 
     (reparse points) and the Data Deduplication store.

Applications that call the 
    <a href="/previous-versions/windows/desktop/api/ddpbackup/nf-ddpbackup-idedupbackupsupport-restorefiles">RestoreFiles</a> method must also implement 
    the <a href="/previous-versions/windows/desktop/api/ddpbackup/nn-ddpbackup-idedupreadfilecallback">IDedupReadFileCallback</a> interface. Before 
    calling the <b>RestoreFiles</b> method, the 
    application must have previously restored the Data Deduplication reparse points for the files to the location 
    specified by the <i>FileFullPaths</i> parameter. Metadata located in the reparse points will be 
    utilized by Data Deduplication to further drive the restore process.

After calling this method, applications can expect to receive two calls to 
    <a href="/previous-versions/windows/desktop/api/ddpbackup/nf-ddpbackup-idedupreadfilecallback-ordercontainersrestore">IDedupReadFileCallback::OrderContainersRestore</a> 
    (one for stream map containers and one for data containers) and two or more calls to 
    <a href="/previous-versions/windows/desktop/api/ddpbackup/nf-ddpbackup-idedupreadfilecallback-readbackupfile">IDedupReadFileCallback::ReadBackupFile</a>. 
    The application will also receive one call to 
    <a href="/previous-versions/windows/desktop/api/ddpbackup/nf-ddpbackup-idedupreadfilecallback-previewcontainerread">IDedupReadFileCallback::PreviewContainerRead</a> 
    before each call to 
    <b>ReadBackupFile</b> that is directed 
    to a container file.

## -parameters

### -param NumberOfFiles [in]

The number of files to restore. If this exceeds 10,000 then the method will fail with 
      <b>E_INVALIDARG</b> (0x80070057).

### -param FileFullPaths [in]

For each file, this parameter contains the full path from the root directory of the volume to the reparse 
      point previously restored by the application.

### -param Store [in]

<a href="/previous-versions/windows/desktop/api/ddpbackup/nn-ddpbackup-idedupreadfilecallback">IDedupReadFileCallback</a> interface pointer 
      for the backup store. This parameter is required and cannot be <b>NULL</b>.

### -param Flags [in]

This parameter must be <b>DEDUP_RECONSTRUCT_UNOPTIMIZED</b> on input. For more 
      information, see the 
      <a href="/windows/win32/api/ddpbackup/ne-ddpbackup-dedup_backup_support_param_type">DEDUP_BACKUP_SUPPORT_PARAM_TYPE</a> 
       enumeration.

### -param FileResults [out]

For each file, this parameter contains the results of the restore operation for that file. This parameter 
      is optional and can be <b>NULL</b> if the application doesn't need to know the results for each individual file.



#### S_OK (0x00000000L)

The file was restored successfully.



#### S_FALSE (0x00000001L)

The specified file is not a deduplicated file.



#### DDP_E_FILE_CORRUPT (0x80565355L)

Data deduplication encountered a file corruption error.



#### DDP_E_FILE_SYSTEM_CORRUPT (0x8056530EL)

Data deduplication encountered a file system corruption error.



#### DDP_E_INVALID_DATA (0x8056531DL)

The data is not valid.



#### DDP_E_JOB_COMPLETED_PARTIAL_SUCCESS (0x80565356L)

The operation completed with some errors. Check the event logs for more details.

<b>Windows Server 2012:  </b>This value is not supported before Windows Server 2012 R2.



#### DDP_E_NOT_FOUND (0x80565301L)

The requested object was not found.



#### DDP_E_PATH_NOT_FOUND (0x80565304L)

A specified container path was not found in the backup store.



#### DDP_E_UNEXPECTED (0x8056530CL)

Data deduplication encountered an unexpected error. Check the Data Deduplication Operational event log 
        for more information.



#### DDP_E_VOLUME_DEDUP_DISABLED (0x80565323L)

The specified volume is not enabled for deduplication.



#### DDP_E_VOLUME_UNSUPPORTED (0x8056530bL)

The specified volume type is not supported. Deduplication is supported on fixed, write-enabled NTFS data 
         volumes.

<b>Windows Server 2012:  </b>This value is not supported before Windows Server 2012 R2.

## -returns

This method can return standard <b>HRESULT</b> values, such as 
       <b>S_OK</b>. It can also return converted 
       <a href="/windows/desktop/Debug/system-error-codes">system error codes</a> using the 
       <a href="/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. You can test for success 
       or failure <b>HRESULT</b> values by using the 
       <a href="/windows/desktop/api/winerror/nf-winerror-succeeded">SUCCEEDED</a> and 
       <a href="/windows/desktop/api/winerror/nf-winerror-failed">FAILED</a> macros defined in Winerror.h. Possible 
       return values include the following.

If no file was restored successfully, the result is the first file error encountered. This will be one of the 
       "DDP_E_<i>XXX</i>" error codes above.

## -remarks

The <i>Store</i> parameter is required because the restore engine (implemented by Data 
    Deduplication) can read data from the backup media only by calling the 
    <a href="/previous-versions/windows/desktop/api/ddpbackup/nf-ddpbackup-idedupreadfilecallback-readbackupfile">IDedupReadFileCallback::ReadBackupFile</a> 
    method.

## -see-also

<a href="/windows/win32/api/ddpbackup/ne-ddpbackup-dedup_backup_support_param_type">DEDUP_BACKUP_SUPPORT_PARAM_TYPE</a>



<a href="/previous-versions/windows/desktop/api/ddpbackup/nn-ddpbackup-idedupbackupsupport">IDedupBackupSupport</a>



<a href="/previous-versions/windows/desktop/api/ddpbackup/nn-ddpbackup-idedupreadfilecallback">IDedupReadFileCallback</a>