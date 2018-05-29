---
UID: NF:ddpbackup.IDedupBackupSupport.RestoreFiles
title: IDedupBackupSupport::RestoreFiles
author: windows-sdk-content
description: Reconstructs a set of files from a backup store that contains the fully optimized version of the files (reparse points) and the Data Deduplication store.
old-location: dedup\idedupbackupsupport_restorefiles.htm
old-project: dedup
ms.assetid: CFBB0B59-2869-4A30-8F2F-A473372B1E68
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: DDP_E_FILE_CORRUPT, DDP_E_FILE_SYSTEM_CORRUPT, DDP_E_INVALID_DATA, DDP_E_JOB_COMPLETED_PARTIAL_SUCCESS, DDP_E_NOT_FOUND, DDP_E_PATH_NOT_FOUND, DDP_E_UNEXPECTED, DDP_E_VOLUME_DEDUP_DISABLED, DDP_E_VOLUME_UNSUPPORTED, IDedupBackupSupport interface [Data Deduplication API],RestoreFiles method, IDedupBackupSupport.RestoreFiles, IDedupBackupSupport::RestoreFiles, RestoreFiles, RestoreFiles method [Data Deduplication API], RestoreFiles method [Data Deduplication API],IDedupBackupSupport interface, S_FALSE, S_OK, ddpbackup/IDedupBackupSupport::RestoreFiles, dedup.idedupbackupsupport_restorefile, dedup.idedupbackupsupport_restorefiles
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
req.typenames: DEDUP_BACKUP_SUPPORT_PARAM_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	DdpBackup.h
api_name:
-	IDedupBackupSupport.RestoreFiles
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDedupBackupSupport::RestoreFiles


## -description


Reconstructs a set of files from a backup store that contains the fully optimized version of the files 
     (reparse points) and the Data Deduplication store.

Applications that call the 
    <a href="dedup.idedupbackupsupport_restorefile">RestoreFiles</a> method must also implement 
    the <a href="https://msdn.microsoft.com/0B7F5A5B-EB60-4BAF-86AF-D9101F3B482C">IDedupReadFileCallback</a> interface. Before 
    calling the <b>RestoreFiles</b> method, the 
    application must have previously restored the Data Deduplication reparse points for the files to the location 
    specified by the <i>FileFullPaths</i> parameter. Metadata located in the reparse points will be 
    utilized by Data Deduplication to further drive the restore process.

After calling this method, applications can expect to receive two calls to 
    <a href="https://msdn.microsoft.com/25871056-5833-40DA-9C5B-690DCAB16E5C">IDedupReadFileCallback::OrderContainersRestore</a> 
    (one for stream map containers and one for data containers) and two or more calls to 
    <a href="https://msdn.microsoft.com/9A85B32B-7430-46AC-A9BF-2896651F40AF">IDedupReadFileCallback::ReadBackupFile</a>. 
    The application will also receive one call to 
    <a href="https://msdn.microsoft.com/A3AFB530-ED97-4BEC-BF9D-668115E36A36">IDedupReadFileCallback::PreviewContainerRead</a> 
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


<a href="https://msdn.microsoft.com/0B7F5A5B-EB60-4BAF-86AF-D9101F3B482C">IDedupReadFileCallback</a> interface pointer 
      for the backup store. This parameter is required and cannot be <b>NULL</b>.


### -param Flags [in]

This parameter must be <b>DEDUP_RECONSTRUCT_UNOPTIMIZED</b> on input. For more 
      information, see the 
      <a href="https://msdn.microsoft.com/654663C4-1E28-435A-9D81-1E390BC66B62">DEDUP_BACKUP_SUPPORT_PARAM_TYPE</a> 
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
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a> using the 
       <a href="_com_hresult_from_win32">HRESULT_FROM_WIN32</a> macro. You can test for success 
       or failure <b>HRESULT</b> values by using the 
       <a href="_com_succeeded">SUCCEEDED</a> and 
       <a href="_com_failed">FAILED</a> macros defined in Winerror.h. Possible 
       return values include the following.

If no file was restored successfully, the result is the first file error encountered. This will be one of the 
       "DDP_E_<i>XXX</i>" error codes above.




## -remarks



The <i>Store</i> parameter is required because the restore engine (implemented by Data 
    Deduplication) can read data from the backup media only by calling the 
    <a href="https://msdn.microsoft.com/9A85B32B-7430-46AC-A9BF-2896651F40AF">IDedupReadFileCallback::ReadBackupFile</a> 
    method.




## -see-also




<a href="https://msdn.microsoft.com/654663C4-1E28-435A-9D81-1E390BC66B62">DEDUP_BACKUP_SUPPORT_PARAM_TYPE</a>



<a href="https://msdn.microsoft.com/45AACC37-3C83-4DBA-8C18-26D76ED831BB">IDedupBackupSupport</a>



<a href="https://msdn.microsoft.com/0B7F5A5B-EB60-4BAF-86AF-D9101F3B482C">IDedupReadFileCallback</a>
 

 

