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

# BackupRead function


## -description


The <b>BackupRead</b> function can be used to back up 
    a file or directory, including the security information. The function reads data associated with a 
    specified file or directory into a buffer, which can then be written to the backup medium using the 
    <a href="https://msdn.microsoft.com/9d6fa723-fe3e-4052-b0b3-2686eee076a7">WriteFile</a> function.


## -parameters




### -param hFile [in]

Handle to the file or directory to be backed up. To obtain the handle, call the 
      <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> function. The SACLs are not read unless the 
      file handle was created with the <b>ACCESS_SYSTEM_SECURITY</b> access right. For more 
      information, see <a href="https://msdn.microsoft.com/991d7d94-fae7-406f-b2e3-dee811279366">File Security and Access 
      Rights</a>.

The handle must be synchronous (nonoverlapped). This means that the <b>FILE_FLAG_OVERLAPPED</b> flag must not be set when <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> is called. This function does not validate that the handle it receives is synchronous, so it does not return an error code for a synchronous handle, but calling it with an asynchronous (overlapped) handle can result in subtle errors that are very difficult to debug.

The <b>BackupRead</b> function may fail if 
      <b>CreateFile</b> was called with the flag 
      <b>FILE_FLAG_NO_BUFFERING</b>. In this case, the 
      <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function returns the value 
      <b>ERROR_INVALID_PARAMETER</b>.


### -param lpBuffer [out]

Pointer to a buffer that receives the data.


### -param nNumberOfBytesToRead [in]

Length of the buffer, in bytes. The buffer size must be greater than the size of a 
      <a href="https://msdn.microsoft.com/8beb4315-ec0e-4f6f-abfe-369094f7bedd">WIN32_STREAM_ID</a> structure.


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
       error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function is not intended for use in backing up files encrypted under the 
    Encrypted File System. Use 
    <a href="https://msdn.microsoft.com/15f6f617-969d-4a40-9038-b902a3c2518b">ReadEncryptedFileRaw</a> for that purpose.

If an error occurs while <b>BackupRead</b> is reading data, 
    the calling process can skip the bad data by calling the 
    <a href="https://msdn.microsoft.com/d5ffba3d-f744-49b4-83e0-e32bd45ecc4c">BackupSeek</a> function.

The file or directory should be restored using the 
    <a href="https://msdn.microsoft.com/92befb48-68eb-4af3-b58a-c5e17bf14098">BackupWrite</a> function.




## -see-also




<a href="https://msdn.microsoft.com/d5ffba3d-f744-49b4-83e0-e32bd45ecc4c">BackupSeek</a>



<a href="https://msdn.microsoft.com/92befb48-68eb-4af3-b58a-c5e17bf14098">BackupWrite</a>



<a href="https://msdn.microsoft.com/a2d367e1-13a9-47a8-8329-6e550c09ad58">Creating a Backup Application</a>



<a href="https://msdn.microsoft.com/15f6f617-969d-4a40-9038-b902a3c2518b">ReadEncryptedFileRaw</a>



<a href="https://msdn.microsoft.com/8beb4315-ec0e-4f6f-abfe-369094f7bedd">WIN32_STREAM_ID</a>
 

 

