---
UID: NF:winbase.BackupWrite
title: BackupWrite function (winbase.h)
description: Restore a file or directory that was backed up using BackupRead.
helpviewer_keywords: ["BackupWrite","BackupWrite function [Backup]","_win32_backupwrite","backup.backupwrite","base.backupwrite","winbase/BackupWrite"]
old-location: backup\backupwrite.htm
tech.root: Backup
ms.assetid: 92befb48-68eb-4af3-b58a-c5e17bf14098
ms.date: 12/05/2018
ms.keywords: BackupWrite, BackupWrite function [Backup], _win32_backupwrite, backup.backupwrite, base.backupwrite, winbase/BackupWrite
req.header: winbase.h
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BackupWrite
 - winbase/BackupWrite
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-kernel32-legacy-l1-1-6.dll
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - BackupWrite
---

# BackupWrite function


## -description

The <b>BackupWrite</b> function can be used to 
    restore a file or directory that was backed up using 
    <a href="/windows/desktop/api/winbase/nf-winbase-backupread">BackupRead</a>. Use the 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-readfile">ReadFile</a> function to get a stream of data from the backup 
    medium, then use <b>BackupWrite</b> to write the data to the specified file or 
    directory.

## -parameters

### -param hFile [in]

Handle to the file or directory to be restored. To obtain the handle, call the <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function. The SACLs are not restored unless the file handle was created with the <b>ACCESS_SYSTEM_SECURITY</b> access right. To ensure that the integrity ACEs are restored correctly, the file handle must also have been created with the <b>WRITE_OWNER</b> access right. For more information, see [File security and access rights](/windows/win32/fileio/file-security-and-access-rights).

The handle must be synchronous (nonoverlapped). This means that the <b>FILE_FLAG_OVERLAPPED</b> flag must not be set when <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> is called. This function does not validate that the handle it receives is synchronous, so it does not return an error code for a synchronous handle, but calling it with an asynchronous (overlapped) handle can result in subtle errors that are very difficult to debug.

The <b>BackupWrite</b> function may fail if 
      <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> was called with the flag 
      <b>FILE_FLAG_NO_BUFFERING</b>. In this case, the 
      <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function returns the value
      <b>ERROR_INVALID_PARAMETER</b>.

### -param lpBuffer [in]

Pointer to a buffer that the function writes data from.

### -param nNumberOfBytesToWrite [in]

Size of the buffer, in bytes. The buffer size must be greater than the size of a 
      <a href="/windows/desktop/api/winbase/ns-winbase-win32_stream_id">WIN32_STREAM_ID</a> structure.

### -param lpNumberOfBytesWritten [out]

Pointer to a variable that receives the number of bytes written.

### -param bAbort [in]

Indicates whether you have finished using <b>BackupWrite</b> on the handle. 
      While you are restoring the file, specify this parameter as <b>FALSE</b>. After you are done 
      using <b>BackupWrite</b>, you must call <b>BackupWrite</b> 
      one more time specifying <b>TRUE</b> for this parameter and passing the appropriate 
      <i>lpContext</i>. <i>lpContext</i> must be passed when 
      <i>bAbort</i> is <b>TRUE</b>; all other parameters are ignored.

### -param bProcessSecurity [in]

Specifies whether the function will restore the access-control list (ACL) data for the file or directory.

If <i>bProcessSecurity</i> is <b>TRUE</b>, you need to specify 
      <b>WRITE_OWNER</b> and <b>WRITE_DAC</b> access when opening the file or 
      directory handle. If the handle does not have those access rights, the operating system denies access to the 
      ACL data, and ACL data restoration will not occur.

### -param lpContext [out]

Pointer to a variable that receives a pointer to an internal data structure used by 
      <b>BackupWrite</b> to maintain context information during a restore operation.

You must set the variable pointed to by <i>lpContext</i> to <b>NULL</b> 
      before the first call to <b>BackupWrite</b> for the specified file or directory. The 
      function allocates memory for the data structure, and then sets the variable to point to that structure. You 
      must not change <i>lpContext</i> or the variable that it points to between calls to 
      <b>BackupWrite</b>.

To release the memory used by the data structure, call <b>BackupWrite</b> with the 
      <i>bAbort</i> parameter set to <b>TRUE</b> when the restore operation is 
      complete.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero, indicating that an I/O error occurred. To get extended 
       error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function is not intended for use in restoring files encrypted under the 
    <a href="/windows/desktop/FileIO/file-encryption">Encrypted File System</a>. Use 
    <a href="/windows/desktop/api/winbase/nf-winbase-writeencryptedfileraw">WriteEncryptedFileRaw</a> for that purpose.

The data read from the backup medium must be substreams separated by 
    <a href="/windows/desktop/api/winbase/ns-winbase-win32_stream_id">WIN32_STREAM_ID</a> structures.

The <b>BACKUP_LINK</b> stream type lets you restore files with hard links.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-backupread">BackupRead</a>



<a href="/windows/desktop/api/winbase/nf-winbase-backupseek">BackupSeek</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/api/winbase/ns-winbase-win32_stream_id">WIN32_STREAM_ID</a>



<a href="/windows/desktop/api/winbase/nf-winbase-writeencryptedfileraw">WriteEncryptedFileRaw</a>