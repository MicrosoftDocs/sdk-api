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

# _FILE_NOTIFY_INFORMATION structure


## -description


Describes the changes found by the 
    <a href="https://msdn.microsoft.com/14dfc93d-557e-43d0-be45-8414cfd92c29">ReadDirectoryChangesW</a> function.


## -struct-fields




### -field NextEntryOffset

The number of bytes that must be skipped to get to the next record. A value of zero indicates that this is 
      the last record.


### -field Action

The type of change that has occurred. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FILE_ACTION_ADDED"></a><a id="file_action_added"></a><dl>
<dt><b>FILE_ACTION_ADDED</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The file was added to the directory.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_ACTION_REMOVED"></a><a id="file_action_removed"></a><dl>
<dt><b>FILE_ACTION_REMOVED</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The file was removed from the directory.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_ACTION_MODIFIED"></a><a id="file_action_modified"></a><dl>
<dt><b>FILE_ACTION_MODIFIED</b></dt>
<dt>0x00000003</dt>
</dl>
</td>
<td width="60%">
The file was modified. This can be a change in the time stamp or attributes.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_ACTION_RENAMED_OLD_NAME"></a><a id="file_action_renamed_old_name"></a><dl>
<dt><b>FILE_ACTION_RENAMED_OLD_NAME</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The file was renamed and this is the old name.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_ACTION_RENAMED_NEW_NAME"></a><a id="file_action_renamed_new_name"></a><dl>
<dt><b>FILE_ACTION_RENAMED_NEW_NAME</b></dt>
<dt>0x00000005</dt>
</dl>
</td>
<td width="60%">
The file was renamed and this is the new name.

</td>
</tr>
</table>
 


### -field FileNameLength

The size of the file name portion of the record, in bytes. Note that this value does not include the 
      terminating null character.


### -field FileName

A variable-length field that contains the file name relative to the directory handle. The file name is in 
      the Unicode character format and is not null-terminated.
	     

If there is both a short and long name for the file, the function will return one of these names, but it is 
 	     unspecified which one.


## -see-also




<a href="https://msdn.microsoft.com/14dfc93d-557e-43d0-be45-8414cfd92c29">ReadDirectoryChangesW</a>
 

 

