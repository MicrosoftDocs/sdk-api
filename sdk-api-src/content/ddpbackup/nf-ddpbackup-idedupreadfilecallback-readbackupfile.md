---
UID: NF:ddpbackup.IDedupReadFileCallback.ReadBackupFile
title: IDedupReadFileCallback::ReadBackupFile (ddpbackup.h)
description: Reads data from a Data Deduplication store metadata or container file located in the backup store.
helpviewer_keywords: ["IDedupReadFileCallback interface [Data Deduplication API]","ReadBackupFile method","IDedupReadFileCallback.ReadBackupFile","IDedupReadFileCallback::ReadBackupFile","ReadBackupFile","ReadBackupFile method [Data Deduplication API]","ReadBackupFile method [Data Deduplication API]","IDedupReadFileCallback interface","ddpbackup/IDedupReadFileCallback::ReadBackupFile","dedup.idedupreadfilecallback_readbackupfile"]
old-location: dedup\idedupreadfilecallback_readbackupfile.htm
tech.root: dedup
ms.assetid: 9A85B32B-7430-46AC-A9BF-2896651F40AF
ms.date: 12/05/2018
ms.keywords: IDedupReadFileCallback interface [Data Deduplication API],ReadBackupFile method, IDedupReadFileCallback.ReadBackupFile, IDedupReadFileCallback::ReadBackupFile, ReadBackupFile, ReadBackupFile method [Data Deduplication API], ReadBackupFile method [Data Deduplication API],IDedupReadFileCallback interface, ddpbackup/IDedupReadFileCallback::ReadBackupFile, dedup.idedupreadfilecallback_readbackupfile
req.header: ddpbackup.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDedupReadFileCallback::ReadBackupFile
 - ddpbackup/IDedupReadFileCallback::ReadBackupFile
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
 - IDedupReadFileCallback.ReadBackupFile
---

# IDedupReadFileCallback::ReadBackupFile


## -description

 Reads data from a Data Deduplication store metadata or  container file located  in the backup store.

## -parameters

### -param FileFullPath [in]

The full path from the root directory of the volume to the container file.

### -param FileOffset [in]

The offset, in bytes, from the beginning of the file to the beginning of the data to be read.

### -param SizeToRead [in]

The number of bytes to read from the file.

### -param FileBuffer [out]

A pointer to a buffer that receives the data that is read from the file. The size of the buffer must be greater than or equal to the number specified in the <i>SizeToRead</i> parameter.

### -param ReturnedSize [out]

Pointer to a ULONG variable that receives the number of bytes that were read from the backup store. If the call to <b>ReadBackupFile</b> is successful, this number is equal to the value that was specified in the <i>SizeToRead</i> parameter.

### -param Flags [in]

This parameter is reserved for future use.

## -returns

This method can return standard <b>HRESULT</b> values, such as <b>S_OK</b>. It can also return converted <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Possible return values include the following.

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/previous-versions/windows/desktop/api/ddpbackup/nn-ddpbackup-idedupreadfilecallback">IDedupReadFileCallback</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-readfile">ReadFile</a>