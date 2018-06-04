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

# SHCreateDirectoryExW function


## -description


<p class="CCE_Message">[This function is available through Windows XP Service Pack 2 (SP2) and Windows Server 2003. It might be altered or unavailable in subsequent versions of Windows.]

Creates a new file system folder, with optional security attributes.


## -parameters




### -param hwnd [in, optional]

Type: <b>HWND</b>

A handle to a parent window. This parameter can be set to <b>NULL</b> if no user interface will be displayed.


### -param pszPath [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string specifying the fully qualified path of the directory. This string is of maximum length of 248 characters, including the terminating null character.


### -param psa [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a>*</b>

 A pointer to a <a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a> structure with the directory's security attribute. Set this parameter to <b>NULL</b> if no security attributes need to be set.


## -returns



Type: <b>int</b>

Returns <b>ERROR_SUCCESS</b> if successful. If the operation fails, other error codes can be returned, including those listed here. For values not specifically listed, see <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_PATHNAME</b></dt>
</dl>
</td>
<td width="60%">
The <i>pszPath</i> parameter was set to a relative path.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILENAME_EXCED_RANGE</b></dt>
</dl>
</td>
<td width="60%">
The path pointed to by <i>pszPath</i> is too long.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_PATH_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The system cannot find the path pointed to by <i>pszPath</i>. The path may contain an invalid entry.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
The directory exists.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ALREADY_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
The directory exists.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANCELLED</b></dt>
</dl>
</td>
<td width="60%">
The user canceled the operation.

</td>
</tr>
</table>
 




## -remarks



This function creates a file system folder whose fully qualified path is given by <i>pszPath</i>. If one or more of the intermediate folders do not exist, they are created as well. <b>SHCreateDirectoryEx</b> also verifies that the files are visible. If they are not visible, expect one of the following:

				

<ul>
<li>If <i>hwnd</i> is set to a valid window handle, a message box is displayed warning the user that he or she might not be able to access the files. If the user chooses not to proceed, the function returns <b>ERROR_CANCELLED</b>.</li>
<li>If <i>hwnd</i> is set to <b>NULL</b>, no user interface is displayed and the function returns <b>ERROR_CANCELLED</b>.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/4927429c-f457-4dda-aa0d-236eb236795c">SHCreateDirectory</a>
 

 

