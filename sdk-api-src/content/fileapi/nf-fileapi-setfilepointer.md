---
UID: NF:fileapi.SetFilePointer
title: SetFilePointer function (fileapi.h)
author: windows-sdk-content
description: Moves the file pointer of the specified file.
old-location: fs\setfilepointer.htm
tech.root: FileIO
ms.assetid: a0a0081b-9132-4dea-967b-1ee1d1fdfa13
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FILE_BEGIN, FILE_CURRENT, FILE_END, SetFilePointer, SetFilePointer function [Files], _win32_setfilepointer, base.setfilepointer, fileapi/SetFilePointer, fs.setfilepointer, winbase/SetFilePointer
ms.topic: function
req.header: fileapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-File-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-File-l1-2-0.dll
 - API-MS-Win-Core-File-l1-2-1.dll
 - API-MS-Win-Core-File-l1-2-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - SetFilePointer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetFilePointer function


## -description


Moves the file pointer of the specified file.

This function stores the file pointer in two <b>LONG</b> values. To work with file pointers
     that are larger than a single <b>LONG</b> value, it is easier to use the 
     <a href="https://msdn.microsoft.com/a6fdfa00-626d-425d-b00e-c174b19ea4b9">SetFilePointerEx</a> function.


## -parameters




### -param hFile [in]

A handle to the file.
      

The file handle must be created with the <b>GENERIC_READ</b> or 
       <b>GENERIC_WRITE</b> access right. For more information, see 
       <a href="https://msdn.microsoft.com/991d7d94-fae7-406f-b2e3-dee811279366">File Security and Access Rights</a>.


### -param lDistanceToMove [in]

The low order 32-bits of a signed value that specifies the number of bytes to move the file pointer.
      

If <i>lpDistanceToMoveHigh</i> is not <b>NULL</b>, 
       <i>lpDistanceToMoveHigh</i> and <i>lDistanceToMove</i> form a single 
       64-bit signed value that specifies the distance to move.

If <i>lpDistanceToMoveHigh</i> is <b>NULL</b>, 
       <i>lDistanceToMove</i> is a 32-bit signed value. A positive value for 
       <i>lDistanceToMove</i> moves the file pointer forward in the file, and a negative value 
       moves the file pointer back.


### -param lpDistanceToMoveHigh [in, out, optional]

A pointer to the high order 32-bits of the signed 64-bit distance to move.
      

If you do not need the high order 32-bits, this pointer must be set to <b>NULL</b>.

When  not <b>NULL</b>, this parameter also receives the high order 
       <b>DWORD</b> of the new value of the file pointer. For more information, see the Remarks 
       section in this topic.


### -param dwMoveMethod [in]

The starting point for the file pointer move.
      

This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FILE_BEGIN"></a><a id="file_begin"></a><dl>
<dt><b>FILE_BEGIN</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The starting point is zero or the beginning of the file.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_CURRENT"></a><a id="file_current"></a><dl>
<dt><b>FILE_CURRENT</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The starting point is the current value of the file pointer.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_END"></a><a id="file_end"></a><dl>
<dt><b>FILE_END</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The starting point is the current end-of-file position.

</td>
</tr>
</table>
 


## -returns



If the function succeeds and <i>lpDistanceToMoveHigh</i> is 
       <b>NULL</b>, the return value is the low-order <b>DWORD</b> of the new 
       file pointer.
       <b>Note</b>  If the function returns a value other than <b>INVALID_SET_FILE_POINTER</b>, the call 
         to <b>SetFilePointer</b> has succeeded. You do not need to 
         call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.



If function succeeds and <i>lpDistanceToMoveHigh</i> is not 
       <b>NULL</b>, the return value is the low-order <b>DWORD</b> of the new 
       file pointer and <i>lpDistanceToMoveHigh</i> contains the high order 
       <b>DWORD</b> of the new file pointer.

If the function fails, the return value is <b>INVALID_SET_FILE_POINTER</b>. To get 
       extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

If a new file pointer is a negative value, the function fails, the file pointer is not moved, and the code 
       returned by <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> is 
       <b>ERROR_NEGATIVE_SEEK</b>.

If <i>lpDistanceToMoveHigh</i> is <b>NULL</b> and the new file position 
       does not fit in a 32-bit value, the function fails and returns 
       <b>INVALID_SET_FILE_POINTER</b>.

<div class="alert"><b>Note</b>  Because <b>INVALID_SET_FILE_POINTER</b> is a valid value for the 
       low-order <b>DWORD</b> of the new file pointer, you must check both the return value of 
       the function and the error code returned by 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> to determine whether or not an error has 
       occurred. If an error has occurred, the return value of 
       <b>SetFilePointer</b> is 
       <b>INVALID_SET_FILE_POINTER</b> and 
       <b>GetLastError</b> returns a value other than 
       <b>NO_ERROR</b>. For a code example that demonstrates how to check for failure, see the 
       Remarks section in this topic.</div>
<div> </div>



## -remarks



The file pointer that is identified by the value of the <i>hFile</i> parameter is not used 
    for overlapped read and write operations. 

The <i>hFile</i> parameter must refer to a file stored on a seeking device; for example, a disk volume. Calling the 
    <b>SetFilePointer</b> function with a handle to a non-seeking 
    device such as a pipe or a communications device is not supported, even though the 
    <b>SetFilePointer</b> function may not return an error. The behavior of the 
    <b>SetFilePointer</b> function in this case is undefined.

<p class="proch"><img alt="" src="../common/wedge.gif"/><b>To specify the offset for overlapped operations</b>

<ul>
<li>Use the <b>Offset</b> and <b>OffsetHigh</b> members of the 
      <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure.</li>
</ul>
<p class="proch"><img alt="" src="../common/wedge.gif"/><b>To determine the file type for <i>hFile</i></b>

<ul>
<li>Use the <a href="https://msdn.microsoft.com/11760e2f-5e8b-4ec7-959b-fb23d5d9a0aa">GetFileType</a> function.</li>
</ul>
For information about how to determine the position of a file pointer, see 
    <a href="https://msdn.microsoft.com/21c75d96-0357-422d-b12b-74c56f64ecf1">Positioning a File Pointer</a>.

Be careful when you set a file pointer in a multithreaded application. You must synchronize access to shared 
    resources. For example, an application with threads that share a file handle, update the file pointer, and read 
    from the file must protect this sequence by using a critical section object or mutex object. For more information, 
    see <a href="https://msdn.microsoft.com/2ec11a42-3d12-4d60-9dd7-dc38926d56e1">Critical Section Objects</a> and 
    <a href="https://msdn.microsoft.com/eca0795a-1fd0-4034-9d61-9416670919cf">Mutex Objects</a>.

If the <i>hFile</i> handle is opened with the 
    <b>FILE_FLAG_NO_BUFFERING</b> flag set, an application can move the file pointer only to 
    sector-aligned positions. A sector-aligned position is a position that is a whole number multiple of the volume 
    sector size. An application can obtain a volume sector size by calling the 
    <a href="https://msdn.microsoft.com/4fe14c49-3fd6-48b7-92de-a0c867b2e042">GetDiskFreeSpace</a> function.

If an application calls <b>SetFilePointer</b> with distance 
     to move values that result in a position not sector-aligned and a handle that is opened with 
     <b>FILE_FLAG_NO_BUFFERING</b>, the function fails, and 
     <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns 
      <b>ERROR_INVALID_PARAMETER</b>.

It is not an error to set a file pointer to a position beyond the end of the file. The size of the file does 
    not increase until you call the <a href="https://msdn.microsoft.com/2a579609-144a-4b77-8605-87aecf1f0957">SetEndOfFile</a>, 
    <a href="https://msdn.microsoft.com/9d6fa723-fe3e-4052-b0b3-2686eee076a7">WriteFile</a>, or 
    <a href="https://msdn.microsoft.com/6995c4ee-ba91-41d5-b72d-19dc2eb95945">WriteFileEx</a> function. A write operation increases the size 
    of the file to the file pointer position plus the size of the buffer written, which results in the intervening 
    bytes uninitialized.

If the return value is <b>INVALID_SET_FILE_POINTER</b> and if 
    <i>lpDistanceToMoveHigh</i> is non-<b>NULL</b>, an application must call 
    <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> to determine whether or not the function has 
    succeeded or failed. The following code example shows you that scenario.


```cpp
  // Case One: calling the function with lpDistanceToMoveHigh == NULL 

  // Try to move hFile file pointer some distance  
  DWORD dwPtr = SetFilePointer( hFile, 
                                lDistance, 
                                NULL, 
                                FILE_BEGIN ); 
   
  if (dwPtr == INVALID_SET_FILE_POINTER) // Test for failure
   { 
    // Obtain the error code. 
    DWORD dwError = GetLastError() ; 
   
    // Deal with failure 
    // . . . 
   
   } // End of error handler 


  //
  // Case Two: calling the function with lpDistanceToMoveHigh != NULL

  // Try to move hFile file pointer a huge distance 
  DWORD dwPtrLow = SetFilePointer( hFile, 
                                   lDistLow, 
                                   &lDistHigh, 
                                   FILE_BEGIN ); 
   
  // Test for failure
  if ( dwPtrLow == INVALID_SET_FILE_POINTER && 
       GetLastError() != NO_ERROR )
   {
    // Deal with failure
    // . . .

   } // End of error handler

```


Although the parameter <i>lpDistanceToMoveHigh</i> is used to manipulate huge files, the 
    value of the parameter should be set when moving files of any size. If it is set to 
    <b>NULL</b>, then <i>lDistanceToMove</i> has a maximum value of 
    2^31–2, or 2 gigabytes less 2, because all file pointer values are signed values. Therefore, 
    if there is even a small chance for the file to increase to that size, it is best to treat the file as a huge file 
    and work with 64-bit file pointers. With 
    <a href="https://msdn.microsoft.com/35a9fb47-5a73-479c-8fe0-5a2b07705536">file compression</a> on the NTFS file 
    system, and <a href="https://msdn.microsoft.com/7326041d-f11e-4b80-ac4e-07173e418ce7">sparse files</a>, it is possible to have files that 
    are large even if the underlying volume is not very large.

If <i>lpDistanceToMoveHigh</i> is not <b>NULL</b>, then 
    <i>lpDistanceToMoveHigh</i> and <i>lDistanceToMove</i> form a single 64-bit 
    signed value. The <i>lDistanceToMove</i> parameter is treated as the low-order 32 bits of the 
    value, and <i>lpDistanceToMoveHigh</i> as the high-order 32 bits, which means that 
    <i>lpDistanceToMoveHigh</i> is a sign extension of 
    <i>lDistanceToMove</i>.

To move the file pointer from zero  to 2 gigabytes, <i>lpDistanceToMoveHigh</i> must be 
    set to either <b>NULL</b> or a sign extension of <i>lDistanceToMove</i>. To 
    move the pointer more than 2 gigabytes, use <i>lpDistanceToMoveHigh</i> and 
    <i>lDistanceToMove</i> as a single 64-bit quantity. For example, to move in the range from 2 
    gigabytes to 4 gigabytes set the contents of <i>lpDistanceToMoveHigh</i> to zero, or to 
    –1 for a negative sign extension of <i>lDistanceToMove</i>.

To work with 64-bit file pointers, you can declare a <b>LONG</b>, treat it as the upper 
    half of the 64-bit file pointer, and pass its address in <i>lpDistanceToMoveHigh</i>. This 
    means that you have to treat two different variables as a logical unit, which can cause an error. It is best to 
    use the <b>LARGE_INTEGER</b> structure to create a 64-bit value and pass the two 32-bit 
    values by using the appropriate elements of the union.

Also, it is best to use a function to hide the interface to 
    <b>SetFilePointer</b>. The following code example shows you that 
    scenario.


```cpp
__int64 myFileSeek (HANDLE hf, __int64 distance, DWORD MoveMethod)
{
   LARGE_INTEGER li;

   li.QuadPart = distance;

   li.LowPart = SetFilePointer (hf, 
                                li.LowPart, 
                                &li.HighPart, 
                                MoveMethod);

   if (li.LowPart == INVALID_SET_FILE_POINTER && GetLastError() 
       != NO_ERROR)
   {
      li.QuadPart = -1;
   }

   return li.QuadPart;
}

```


You can use <b>SetFilePointer</b> to determine the length of 
    a file. To do this, use <b>FILE_END</b> for <i>dwMoveMethod</i> and seek to 
    location zero. The file offset returned is the length of the file. However, this practice can have unintended 
    side effects, for example, failure to save the current file pointer so that the program can return to that 
    location. It is best to use <a href="https://msdn.microsoft.com/3f5d2e4a-1e05-41c0-9b7e-0155e212f6dd">GetFileSize</a> instead.

You can also use the <b>SetFilePointer</b> function to query 
    the current file pointer position. To do this, specify a move method of <b>FILE_CURRENT</b> and 
    a distance of zero.

In Windows 8 and Windows Server 2012, this function is supported by the following technologies.

<table>
<tr>
<th>Technology</th>
<th>Supported</th>
</tr>
<tr>
<td>
Server Message Block (SMB) 3.0 protocol

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
SMB 3.0 Transparent Failover (TFO)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
SMB 3.0 with Scale-out File Shares (SO)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
Cluster Shared Volume File System (CsvFS)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
Resilient File System (ReFS)

</td>
<td>
Yes

</td>
</tr>
</table>
 


#### Examples

For a code example of appending files, see 
     <a href="https://msdn.microsoft.com/e4d1f842-16a1-47e4-84b4-9bb44aaa1dc5">Appending One File to Another File</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/4fe14c49-3fd6-48b7-92de-a0c867b2e042">GetDiskFreeSpace</a>



<a href="https://msdn.microsoft.com/3f5d2e4a-1e05-41c0-9b7e-0155e212f6dd">GetFileSize</a>



<a href="https://msdn.microsoft.com/11760e2f-5e8b-4ec7-959b-fb23d5d9a0aa">GetFileType</a>



<a href="https://msdn.microsoft.com/4ad4580d-c002-44a4-a5f6-757e83ed8732">ReadFile</a>



<a href="https://msdn.microsoft.com/6c1a4de1-6cae-4c35-bfba-0bc252fadbd9">ReadFileEx</a>



<a href="https://msdn.microsoft.com/2a579609-144a-4b77-8605-87aecf1f0957">SetEndOfFile</a>



<a href="https://msdn.microsoft.com/a6fdfa00-626d-425d-b00e-c174b19ea4b9">SetFilePointerEx</a>



<a href="https://msdn.microsoft.com/9d6fa723-fe3e-4052-b0b3-2686eee076a7">WriteFile</a>



<a href="https://msdn.microsoft.com/6995c4ee-ba91-41d5-b72d-19dc2eb95945">WriteFileEx</a>
 

 

