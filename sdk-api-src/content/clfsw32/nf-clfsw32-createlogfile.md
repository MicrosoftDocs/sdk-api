---
UID: NF:clfsw32.CreateLogFile
title: CreateLogFile function
author: windows-sdk-content
description: Creates or opens a log.
old-location: fs\createlogfile.htm
tech.root: Clfs
ms.assetid: ac104bf9-7ca7-417a-bd14-09b0e82c6a77
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: CREATE_NEW, CreateLogFile, CreateLogFile function [Files], DELETE, FILE_ATTRIBUTE_ARCHIVE, FILE_FLAG_OVERLAPPED, FILE_SHARE_DELETE, FILE_SHARE_READ, FILE_SHARE_WRITE, GENERIC_READ, GENERIC_WRITE, OPEN_ALWAYS, OPEN_EXISTING, clfsw32/CreateLogFile, fs.createlogfile
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: clfsw32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Clfsw32.lib
req.dll: Clfsw32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Clfsw32.dll
api_name:
 - CreateLogFile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateLogFile function


## -description


Creates or opens a  log. The log can  be dedicated or multiplexed, and that depends on 
   the log name. Use the <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function to close the 
   log.


## -parameters




### -param pszLogFileName [in]

The name of the log.

This  name is specified when creating the log  by using 
       <b>CreateLogFile</b>. The following example identifies the 
       format to use.

<b>log :&lt;</b><i>LogName</i><b>&gt;[::&lt;</b><i>LogStreamName</i><b>&gt;]</b>

For example: The path "LOG:c:\MyDirectory\MyLog" creates the file 
       "c:\MyDirectory\MyLog.blf". The path 
       "\??\LOG:\HarddiskVolume1\MyDirectory\MyLog" creates the file 
       "\\.\HarddiskVolume1\MyDirectory\MyLog.blf", as does the path 
       "\clfs\Device\HarddiskVolume1\MyDirectory\MyLog".

&lt;<i>LogName</i>&gt; corresponds to a valid file path in the file system, and 
       &lt;<i>LogStreamName</i>&gt; is the unique name of a log stream in the log. For more 
       information, see <a href="https://msdn.microsoft.com/a7099979-346c-434d-8af1-6bf1d5a0512f">Log Types</a>.


### -param fDesiredAccess [in]

The type of access that the returned handle has to the log object.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GENERIC_READ"></a><a id="generic_read"></a><dl>
<dt><b>GENERIC_READ</b></dt>
</dl>
</td>
<td width="60%">
Specifies read access to the object.

</td>
</tr>
<tr>
<td width="40%"><a id="GENERIC_WRITE"></a><a id="generic_write"></a><dl>
<dt><b>GENERIC_WRITE</b></dt>
</dl>
</td>
<td width="60%">
Specifies write access to the object.

</td>
</tr>
<tr>
<td width="40%"><a id="DELETE"></a><a id="delete"></a><dl>
<dt><b>DELETE</b></dt>
</dl>
</td>
<td width="60%">
Specify log deletion access

</td>
</tr>
</table>
 

A bitwise <b>OR</b> of two or more of these flags allows combinations of read, write, and delete access to the object.
       <div class="alert"><b>Note</b>  You must specify <b>DELETE</b> access to be able to delete the log.</div>
<div> </div>
<b>Windows Server 2003 R2:  </b>This parameter must be set to <b>GENERIC_WRITE</b>.




### -param dwShareMode [in]

The sharing mode of a file.

A client cannot request a sharing mode that conflicts with any mode that is specified in any previous open 
       request that has an open handle.

If this parameter is zero and the function succeeds, the object cannot be shared and cannot be opened 
       again until the handle is closed.

This parameter can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FILE_SHARE_DELETE"></a><a id="file_share_delete"></a><dl>
<dt><b>FILE_SHARE_DELETE</b></dt>
</dl>
</td>
<td width="60%">
Enables open operations on the object to request delete access. Without this value, other processes 
        cannot open the object  if delete access is requested.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_SHARE_READ"></a><a id="file_share_read"></a><dl>
<dt><b>FILE_SHARE_READ</b></dt>
</dl>
</td>
<td width="60%">
Enables  open operations on the object to request read access. Without this value, other processes cannot 
        open the object if read access is requested.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_SHARE_WRITE"></a><a id="file_share_write"></a><dl>
<dt><b>FILE_SHARE_WRITE</b></dt>
</dl>
</td>
<td width="60%">
Enables open operations on the object to request write access. Without this value, other processes cannot 
        open the object if write access is requested.

</td>
</tr>
</table>
 


### -param psaLogFile [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a> 
      structure that  specifies the security attributes of a log.

It determines whether the returned handle can be 
      inherited by child processes. If this parameter is <b>NULL</b>, the handle cannot be 
      inherited.

The <b>lpSecurityDescriptor</b> member of 
      <a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a> specifies a 
      <a href="https://msdn.microsoft.com/6512d128-3b0c-4ba7-8709-2fd225389a40">security descriptor</a> for the new log 
      handle. If <i>psaLogFile</i> is <b>NULL</b>, the object gets a default 
      security descriptor. The access control lists (ACL) in the default security descriptor for a log come from the 
      primary or impersonation token of the creator.


### -param fCreateDisposition [in]

An action to be taken.

This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CREATE_NEW"></a><a id="create_new"></a><dl>
<dt><b>CREATE_NEW</b></dt>
</dl>
</td>
<td width="60%">
Creates a new file and fails if the file already exists.

</td>
</tr>
<tr>
<td width="40%"><a id="OPEN_EXISTING"></a><a id="open_existing"></a><dl>
<dt><b>OPEN_EXISTING</b></dt>
</dl>
</td>
<td width="60%">
Opens an existing file and fails if the file does not exist.

</td>
</tr>
<tr>
<td width="40%"><a id="OPEN_ALWAYS"></a><a id="open_always"></a><dl>
<dt><b>OPEN_ALWAYS</b></dt>
</dl>
</td>
<td width="60%">
Opens an existing file or creates the file if it does not exist.

</td>
</tr>
</table>
 


### -param fFlagsAndAttributes [in]

The file attributes and flags for the file.

This parameter can take the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FILE_ATTRIBUTE_ARCHIVE"></a><a id="file_attribute_archive"></a><dl>
<dt><b>FILE_ATTRIBUTE_ARCHIVE</b></dt>
</dl>
</td>
<td width="60%">
This non-ephemeral log should be archived.

If this flag is not supplied, the log does not need to be archived, and an archival tail is not maintained 
        for recycling log containers.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_FLAG_OVERLAPPED"></a><a id="file_flag_overlapped"></a><dl>
<dt><b>FILE_FLAG_OVERLAPPED</b></dt>
</dl>
</td>
<td width="60%">
If the <b>FILE_FLAG_OVERLAPPED</b> flag is set, all other flag values are ignored.

Specifying <b>FILE_FLAG_OVERLAPPED</b> means that a file is opened for overlapped I/O, 
        which enables more than one I/O operation to be performed on the log handle. If this flag is set when creating 
        a log, all asynchronous I/O calls to that log must specify an overlapped structure and synchronize with the deferred completion of the call.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value is a handle to the log.

If the function fails, the return value is <b>INVALID_HANDLE_VALUE</b>. To get extended 
      error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

The following list identifies the  possible error codes:




## -see-also




<a href="https://msdn.microsoft.com/f115ee54-3333-4109-8004-d71904a7a943">ACCESS_MASK</a>



<a href="https://msdn.microsoft.com/5e886b96-9431-43f6-b888-e0f47c432371">AddLogContainer</a>



<a href="https://msdn.microsoft.com/b3dec3bd-3e39-42fa-8f73-71784b3d5be2">AddLogContainerSet</a>



<a href="https://msdn.microsoft.com/3788fac0-4e99-49e0-bba1-6a6d22299950">CLFS_CONTAINER_INFORMATION</a>



<a href="https://msdn.microsoft.com/a3059828-d291-493d-a4fe-13d06e49ed12">Common Log File System Functions</a>



<a href="https://msdn.microsoft.com/750c0615-bfac-402b-a590-6c9d800cf2d8">CreateLogMarshallingArea</a>



<a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a>
 

 

