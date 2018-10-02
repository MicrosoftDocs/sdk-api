---
UID: NS:winbase.COPYFILE2_EXTENDED_PARAMETERS
title: COPYFILE2_EXTENDED_PARAMETERS
author: windows-sdk-content
description: Contains extended parameters for the CopyFile2 function.
old-location: fs\copyfile2_extended_parameters.htm
tech.root: fileio
ms.assetid: a8da62e5-bc49-4aff-afaa-e774393b7120
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: COPYFILE2_EXTENDED_PARAMETERS, COPYFILE2_EXTENDED_PARAMETERS structure [Files], COPY_FILE_ALLOW_DECRYPTED_DESTINATION, COPY_FILE_COPY_SYMLINK, COPY_FILE_FAIL_IF_EXISTS, COPY_FILE_NO_BUFFERING, COPY_FILE_NO_OFFLOAD, COPY_FILE_OPEN_SOURCE_FOR_WRITE, COPY_FILE_REQUEST_SECURITY_PRIVILEGES, COPY_FILE_RESTARTABLE, COPY_FILE_RESUME_FROM_PAUSE, fs.copyfile2_extended_parameters, winbase/COPYFILE2_EXTENDED_PARAMETERS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinBase.h
api_name:
 - COPYFILE2_EXTENDED_PARAMETERS
product: Windows
targetos: Windows
req.typenames: COPYFILE2_EXTENDED_PARAMETERS
req.redist: 
---

# COPYFILE2_EXTENDED_PARAMETERS structure


## -description


Contains extended parameters for the <a href="https://msdn.microsoft.com/aa2df686-4b61-4d90-ba0b-c78c5a0d2d59">CopyFile2</a> 
    function.


## -struct-fields




### -field dwSize

Contains the size of this structure, 
      <code>sizeof(COPYFILE2_EXTENDED_PARAMETERS)</code>.


### -field dwCopyFlags

Contains a combination of zero or more of these flag values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="COPY_FILE_ALLOW_DECRYPTED_DESTINATION"></a><a id="copy_file_allow_decrypted_destination"></a><dl>
<dt><b>COPY_FILE_ALLOW_DECRYPTED_DESTINATION</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
The copy will be attempted even if the destination file cannot be encrypted.

</td>
</tr>
<tr>
<td width="40%"><a id="COPY_FILE_COPY_SYMLINK"></a><a id="copy_file_copy_symlink"></a><dl>
<dt><b>COPY_FILE_COPY_SYMLINK</b></dt>
<dt>0x00000800</dt>
</dl>
</td>
<td width="60%">
If the source file is a symbolic link, the destination file is also a symbolic link pointing to the same 
        file as the source symbolic link.

</td>
</tr>
<tr>
<td width="40%"><a id="COPY_FILE_FAIL_IF_EXISTS"></a><a id="copy_file_fail_if_exists"></a><dl>
<dt><b>COPY_FILE_FAIL_IF_EXISTS</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
If the destination file exists the copy operation fails immediately. If a file or directory exists with 
        the destination name then the <a href="https://msdn.microsoft.com/aa2df686-4b61-4d90-ba0b-c78c5a0d2d59">CopyFile2</a> function call will 
        fail with either <code>HRESULT_FROM_WIN32(ERROR_ALREADY_EXISTS)</code> 
        or <code>HRESULT_FROM_WIN32(ERROR_FILE_EXISTS)</code>. If 
        <b>COPY_FILE_RESUME_FROM_PAUSE</b> is also specified then a failure is only triggered if 
        the destination file does not have a valid restart header.

</td>
</tr>
<tr>
<td width="40%"><a id="COPY_FILE_NO_BUFFERING"></a><a id="copy_file_no_buffering"></a><dl>
<dt><b>COPY_FILE_NO_BUFFERING</b></dt>
<dt>0x00001000</dt>
</dl>
</td>
<td width="60%">
The copy is performed using unbuffered I/O, bypassing the system cache resources. This flag is 
        recommended for very large file copies. It is not recommended to pause copies that are using this flag.

</td>
</tr>
<tr>
<td width="40%"><a id="COPY_FILE_NO_OFFLOAD"></a><a id="copy_file_no_offload"></a><dl>
<dt><b>COPY_FILE_NO_OFFLOAD</b></dt>
<dt>0x00040000</dt>
</dl>
</td>
<td width="60%">
Do not attempt to use the Windows Copy Offload mechanism. This is not generally recommended.

</td>
</tr>
<tr>
<td width="40%"><a id="COPY_FILE_OPEN_SOURCE_FOR_WRITE"></a><a id="copy_file_open_source_for_write"></a><dl>
<dt><b>COPY_FILE_OPEN_SOURCE_FOR_WRITE</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The file is copied and the source file is opened for write access.

</td>
</tr>
<tr>
<td width="40%"><a id="COPY_FILE_RESTARTABLE"></a><a id="copy_file_restartable"></a><dl>
<dt><b>COPY_FILE_RESTARTABLE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The file is copied in a manner that can be restarted if the same source and destination filenames are 
        used again. This is slower.

</td>
</tr>
<tr>
<td width="40%"><a id="COPY_FILE_REQUEST_SECURITY_PRIVILEGES"></a><a id="copy_file_request_security_privileges"></a><dl>
<dt><b>COPY_FILE_REQUEST_SECURITY_PRIVILEGES</b></dt>
<dt>0x00002000</dt>
</dl>
</td>
<td width="60%">
The copy is attempted, specifying 
        <code>ACCESS_SYSTEM_SECURITY</code> for the source file and 
         <code>ACCESS_SYSTEM_SECURITY | WRITE_DAC | WRITE_OWNER</code> for the 
         destination file. If these requests are denied the access request will be reduced to the highest privilege 
         level for which access is granted. For more information see 
         <a href="https://msdn.microsoft.com/88198243-dae5-49ac-9d54-bfae7a3a0b1a">SACL Access Right</a>. This can be used to allow the 
         <a href="https://msdn.microsoft.com/d14b5f5b-c353-49e8-82bb-a695a3ec76fd">CopyFile2ProgressRoutine</a> callback to 
         perform operations requiring higher privileges, such as copying the security attributes for the file.

</td>
</tr>
<tr>
<td width="40%"><a id="COPY_FILE_RESUME_FROM_PAUSE"></a><a id="copy_file_resume_from_pause"></a><dl>
<dt><b>COPY_FILE_RESUME_FROM_PAUSE</b></dt>
<dt>0x00004000</dt>
</dl>
</td>
<td width="60%">
The destination file is examined to see if it was copied using 
        <b>COPY_FILE_RESTARTABLE</b>. If so the copy is resumed. If not the file will be fully 
        copied.

</td>
</tr>
</table>
 


### -field pfCancel

If this flag is set to <b>TRUE</b> during the copy operation then the copy operation is 
      canceled.


### -field pProgressRoutine

The optional address of a callback function of type <b>PCOPYFILE2_PROGRESS_ROUTINE</b> that is 
      called each time another portion of the file has been copied. This parameter can be 
      <b>NULL</b>. For more information on the progress callback function, see the 
      <a href="https://msdn.microsoft.com/d14b5f5b-c353-49e8-82bb-a695a3ec76fd">CopyFile2ProgressRoutine</a> callback function.


### -field pvCallbackContext

A pointer to application-specific context information to be passed to the 
      <a href="https://msdn.microsoft.com/d14b5f5b-c353-49e8-82bb-a695a3ec76fd">CopyFile2ProgressRoutine</a>.


## -remarks



To compile an application that uses this structure, define the <b>_WIN32_WINNT</b> 
    macro as <b>_WIN32_WINNT_WIN8</b> or later. For more information, see 
    <a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/aa2df686-4b61-4d90-ba0b-c78c5a0d2d59">CopyFile2</a>



<a href="https://msdn.microsoft.com/d14b5f5b-c353-49e8-82bb-a695a3ec76fd">CopyFile2ProgressRoutine</a>



<a href="https://msdn.microsoft.com/406d5c0f-b49a-4075-ac3e-c5b55a0c3fe9">File Management Structures</a>
 

 

