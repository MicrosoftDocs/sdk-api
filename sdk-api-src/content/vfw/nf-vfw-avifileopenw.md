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

# AVIFileOpenW function


## -description



The <b>AVIFileOpen</b> function opens an AVI file and returns the address of a file interface used to access it. The AVIFile library maintains a count of the number of times a file is opened, but not the number of times it was released. Use the <a href="https://msdn.microsoft.com/c2f94ca2-b46c-48b0-9c31-92cf2cf75be3">AVIFileRelease</a> function to release the file and decrement the count.




## -parameters




### -param ppfile

Pointer to a buffer that receives the new <a href="https://msdn.microsoft.com/401db941-cbf6-452b-84e2-605fafac8a6d">IAVIFile</a> interface pointer.


### -param szFile

Null-terminated string containing the name of the file to open.


### -param uMode

TBD


### -param lpHandler

TBD




#### - mode

Access mode to use when opening the file. The default access mode is OF_READ. The following access modes can be specified with <b>AVIFileOpen</b>.

<table>
<tr>
<th>
Value
</th>
<th>
Meaning
</th>
</tr>
<tr>
<td>OF_CREATE</td>
<td>Creates a new file. If the file already exists, it is truncated to zero length.</td>
</tr>
<tr>
<td>OF_PARSE</td>
<td>Skips time-consuming operations, such as building an index. Set this flag if you want the function to return as quickly as possible—for example, if you are going to query the file properties but not read the file.</td>
</tr>
<tr>
<td>OF_READ</td>
<td>Opens the file for reading.</td>
</tr>
<tr>
<td>OF_READWRITE</td>
<td>Opens the file for reading and writing.</td>
</tr>
<tr>
<td>OF_SHARE_DENY_NONE</td>
<td>Opens the file nonexclusively. Other processes can open the file with read or write access. <b>AVIFileOpen</b> fails if another process has opened the file in compatibility mode.</td>
</tr>
<tr>
<td>OF_SHARE_DENY_READ</td>
<td>Opens the file nonexclusively. Other processes can open the file with write access. <b>AVIFileOpen</b> fails if another process has opened the file in compatibility mode or has read access to it.</td>
</tr>
<tr>
<td>OF_SHARE_DENY_WRITE</td>
<td>Opens the file nonexclusively. Other processes can open the file with read access. <b>AVIFileOpen</b> fails if another process has opened the file in compatibility mode or has write access to it.</td>
</tr>
<tr>
<td>OF_SHARE_EXCLUSIVE</td>
<td>Opens the file and denies other processes any access to it. <b>AVIFileOpen</b> fails if any other process has opened the file.</td>
</tr>
<tr>
<td>OF_WRITE</td>
<td>Opens the file for writing.</td>
</tr>
</table>
 


#### - pclsidHandler

Pointer to a class identifier of the standard or custom handler you want to use. If the value is <b>NULL</b>, the system chooses a handler from the registry based on the file extension or the RIFF type specified in the file.


## -returns



Returns zero if successful or an error otherwise. Possible error values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AVIERR_BADFORMAT</b></dt>
</dl>
</td>
<td width="60%">
The file couldn't be read, indicating a corrupt file or an unrecognized format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AVIERR_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The file could not be opened because of insufficient memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AVIERR_FILEREAD</b></dt>
</dl>
</td>
<td width="60%">
A disk error occurred while reading the file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AVIERR_FILEOPEN</b></dt>
</dl>
</td>
<td width="60%">
A disk error occurred while opening the file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>REGDB_E_CLASSNOTREG</b></dt>
</dl>
</td>
<td width="60%">
According to the registry, the type of file specified in <b>AVIFileOpen</b> does not have a handler to process it.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/89abf60a-1714-4836-93ae-a8a6bf2c24b6">AVIFile Functions</a>



<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>



<a href="https://msdn.microsoft.com/c2f94ca2-b46c-48b0-9c31-92cf2cf75be3">AVIFileRelease</a>
 

 

