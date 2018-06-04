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

# VerFindFileA function


## -description


Determines where to install a file based on whether it locates another version of the file in the system. The values <b>VerFindFile</b> returns in the specified buffers are used in a subsequent call to the <a href="https://msdn.microsoft.com/bd16c1ac-b817-4fb9-bf72-279a8e164f71">VerInstallFile</a> function. 


## -parameters




### -param uFlags

TBD


### -param szFileName [in]

Type: <b>LPCTSTR</b>

The name of the file to be installed. Include only the file name and extension, not a path. 


### -param szWinDir [in, optional]

Type: <b>LPCTSTR</b>

The directory in which Windows is running or will be run. This string is returned by the  <a href="https://msdn.microsoft.com/8c9b55e1-121a-4405-9f83-043752dd48ed">GetWindowsDirectory</a> function. 


### -param szAppDir [in]

Type: <b>LPCTSTR</b>

The directory where the installation program is installing a set of related files. If the installation program is installing an application, this is the directory where the application will reside. This parameter also points to the application's current directory unless otherwise specified. 


### -param szCurDir [out]

Type: <b>LPWSTR</b>

A buffer that receives the path to a current version of the file being installed. The path is a zero-terminated string. If a current version is not installed, the buffer will contain a zero-length string. The buffer should be at least <b>_MAX_PATH</b> characters long, although this is not required. 


### -param puCurDirLen

TBD


### -param szDestDir [out]

Type: <b>LPTSTR</b>

A buffer that receives the path to the installation location recommended by <b>VerFindFile</b>. The path is a zero-terminated string. The buffer should be at least <b>_MAX_PATH</b> characters long, although this is not required. 


### -param puDestDirLen

TBD




#### - dwFlags [in]

Type: <b>DWORD</b>

This parameter can be the following value. All other bits are reserved. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VFFF_ISSHAREDFILE"></a><a id="vfff_issharedfile"></a><dl>
<dt><b>VFFF_ISSHAREDFILE</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
The source file can be shared by multiple applications. An application can use this information to determine where the file should be copied.

</td>
</tr>
</table>
 


#### - lpuCurDirLen [in, out]

Type: <b>PUINT</b>

The length of the 
					<i>szCurDir</i>  buffer. This pointer must not be <b>NULL</b>.

When the function returns, 
					<i>lpuCurDirLen</i> contains the size, in characters, of the data returned in 
					<i>szCurDir</i>, including the terminating null character. If the buffer is too small to contain all the data, 
					<i>lpuCurDirLen</i> will be the size of the buffer required to hold the path.


#### - lpuDestDirLen [in, out]

Type: <b>PUINT</b>

A pointer to a variable that specifies the length of the 
					<i>szDestDir</i> buffer. This pointer must not be <b>NULL</b>.

When the function returns, 
					<i>lpuDestDirLen</i> contains the size, in characters, of the data returned in 
					<i>szDestDir</i>, including the terminating null character. If the buffer is too small to contain all the data, 
					<i>lpuDestDirLen</i> will be the size of the buffer needed to hold the path.


## -returns



Type: <b>DWORD</b>

The return value is a bitmask that indicates the status of the file. It can be one or more of the following values. All other values are reserved.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFF_CURNEDEST</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
The currently installed version of the file is not in the recommended destination.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFF_FILEINUSE</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
The system is using the currently installed version of the file; therefore, the file cannot be overwritten or deleted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFF_BUFFTOOSMALL</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
At least one of the buffers was too small to contain the corresponding string. An application should check the output buffers to determine which buffer was too small.

</td>
</tr>
</table>
 




## -remarks




				 This function works on 16-, 32-, and 64-bit file images.

<b>VerFindFile</b> searches for a copy of the specified file by using the <a href="https://msdn.microsoft.com/800f4d40-252a-44fe-b10d-348c22d69355">OpenFile</a>   function. However, it determines the system directory from the specified Windows directory, or searches the path. 

If the 
				<i>dwFlags</i> parameter indicates that the file is private to this application (not <b>VFFF_ISSHAREDFILE</b>), <b>VerFindFile</b> recommends installing the file in the application's directory. Otherwise, if the system is running a shared copy of the system, the function recommends installing the file in the Windows directory. If the system is running a private copy of the system, the function recommends installing the file in the system directory. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/8c9b55e1-121a-4405-9f83-043752dd48ed">GetWindowsDirectory</a>



<a href="https://msdn.microsoft.com/800f4d40-252a-44fe-b10d-348c22d69355">OpenFile</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/bd16c1ac-b817-4fb9-bf72-279a8e164f71">VerInstallFile</a>



<a href="https://msdn.microsoft.com/60de7900-56b9-4481-bef9-b4079eedf926">Version Information</a>
 

 

