---
UID: NF:winbase.BackupRead
title: BackupRead function (winbase.h)
description: Back up a file or directory, including the security information.
helpviewer_keywords: ["BackupRead","BackupRead function [Backup]","_win32_backupread","backup.backupread","base.backupread","winbase/BackupRead"]
old-location: backup\backupread.htm
tech.root: Backup
ms.assetid: 47d13662-af70-4c76-9fb6-3835e329ae5f
ms.date: 12/05/2018
ms.keywords: BackupRead, BackupRead function [Backup], _win32_backupread, backup.backupread, base.backupread, winbase/BackupRead
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
 - BackupRead
 - winbase/BackupRead
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
 - BackupRead
---

# BackupRead function


## -description

The <b>BackupRead</b> function can be used to back up 
    a file or directory, including the security information. The function reads data associated with a 
    specified file or directory into a buffer, which can then be written to the backup medium using the 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-writefile">WriteFile</a> function.

## -parameters

### -param hFile [in]

Handle to the file or directory to be backed up. To obtain the handle, call the <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function. The SACLs are not read unless the file handle was created with the <b>ACCESS_SYSTEM_SECURITY</b> access right. For more information, see [File security and access rights](/windows/win32/fileio/file-security-and-access-rights).

The handle must be synchronous (nonoverlapped). This means that the <b>FILE_FLAG_OVERLAPPED</b> flag must not be set when <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> is called. This function does not validate that the handle it receives is synchronous, so it does not return an error code for a synchronous handle, but calling it with an asynchronous (overlapped) handle can result in subtle errors that are very difficult to debug.

The <b>BackupRead</b> function may fail if 
      <b>CreateFile</b> was called with the flag 
      <b>FILE_FLAG_NO_BUFFERING</b>. In this case, the 
      <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function returns the value 
      <b>ERROR_INVALID_PARAMETER</b>.

### -param lpBuffer [out]

Pointer to a buffer that receives the data.

### -param nNumberOfBytesToRead [in]

Length of the buffer, in bytes. The buffer size must be greater than the size of a 
      <a href="/windows/desktop/api/winbase/ns-winbase-win32_stream_id">WIN32_STREAM_ID</a> structure.

### -param lpNumberOfBytesRead [out]

Pointer to a variable that receives the number of bytes read.

If the function returns a nonzero value, and the variable pointed to by 
      <i>lpNumberOfBytesRead</i> is zero, then all the data associated with the file handle has 
      been read.

### -param bAbort [in]

Indicates whether you have finished using <b>BackupRead</b> 
      on the handle. While you are backing up the file, specify this parameter as <b>FALSE</b>. 
      Once you are done using <b>BackupRead</b>, you must call 
      <b>BackupRead</b> one more time specifying 
      <b>TRUE</b> for this parameter and passing the appropriate 
      <i>lpContext</i>. <i>lpContext</i> must be passed when 
      <i>bAbort</i> is <b>TRUE</b>; all other parameters are ignored.

### -param bProcessSecurity [in]

Indicates whether the function will restore the access-control list (ACL) data for the file or directory.

If <i>bProcessSecurity</i> is <b>TRUE</b>, the ACL data will be backed 
      up.

### -param lpContext [out]

Pointer to a variable that receives a pointer to an internal data structure used by 
      <b>BackupRead</b> to maintain context information during a 
      backup operation.

You must set the variable pointed to by <i>lpContext</i> to <b>NULL</b> 
      before the first call to <b>BackupRead</b> for the specified 
      file or directory. The function allocates memory for the data structure, and then sets the variable to point to 
      that structure. You must not change <i>lpContext</i> or the variable that it points to 
      between calls to <b>BackupRead</b>.

To release the memory used by the data structure, call 
      <b>BackupRead</b> with the 
      <i>bAbort</i> parameter set to <b>TRUE</b> when the backup operation is complete.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero, indicating that an I/O error occurred. To get extended 
       error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function is not intended for use in backing up files encrypted under the 
    Encrypted File System. Use 
    <a href="/windows/desktop/api/winbase/nf-winbase-readencryptedfileraw">ReadEncryptedFileRaw</a> for that purpose.

If an error occurs while <b>BackupRead</b> is reading data, 
    the calling process can skip the bad data by calling the 
    <a href="/windows/desktop/api/winbase/nf-winbase-backupseek">BackupSeek</a> function.

The file or directory should be restored using the 
    <a href="/windows/desktop/api/winbase/nf-winbase-backupwrite">BackupWrite</a> function.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-backupseek">BackupSeek</a>



<a href="/windows/desktop/api/winbase/nf-winbase-backupwrite">BackupWrite</a>



<a href="/windows/desktop/Backup/creating-a-backup-application">Creating a Backup Application</a>



<a href="/windows/desktop/api/winbase/nf-winbase-readencryptedfileraw">ReadEncryptedFileRaw</a>



<a href="/windows/desktop/api/winbase/ns-winbase-win32_stream_id">WIN32_STREAM_ID</a>