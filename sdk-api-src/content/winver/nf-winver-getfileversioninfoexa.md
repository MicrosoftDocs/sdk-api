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

# GetFileVersionInfoExA function


## -description


Retrieves version information for the specified file.


## -parameters




### -param dwFlags [in]

Type: <b>DWORD</b>

Controls the MUI DLLs (if any) from which the version resource is extracted. The value of this flag must match the flags passed to the corresponding <a href="https://msdn.microsoft.com/e0e841b9-0014-4c7e-a4c7-0478960f962b">GetFileVersionInfoSizeEx</a> call, which was used to determine the buffer size that is passed in the <i>dwLen</i> parameter. Zero or more of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FILE_VER_GET_LOCALISED"></a><a id="file_ver_get_localised"></a><dl>
<dt><b>FILE_VER_GET_LOCALISED</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
Loads the entire version resource (both strings and binary version information) from the corresponding MUI file, if available.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_VER_GET_NEUTRAL"></a><a id="file_ver_get_neutral"></a><dl>
<dt><b>FILE_VER_GET_NEUTRAL</b></dt>
<dt>0x02</dt>
</dl>
</td>
<td width="60%">
Loads the version resource strings from the corresponding MUI file, if available, and loads the binary version information (<b>VS_FIXEDFILEINFO</b>) from the corresponding language-neutral file, if available. 

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_VER_GET_PREFETCHED"></a><a id="file_ver_get_prefetched"></a><dl>
<dt><b>FILE_VER_GET_PREFETCHED</b></dt>
<dt>0x04</dt>
</dl>
</td>
<td width="60%">
Indicates a preference for version.dll to attempt to preload the image outside of the loader lock to avoid contention.  This flag does not change the behavior or semantics of the function.

</td>
</tr>
</table>
 


### -param lpwstrFilename

TBD


### -param dwHandle

Type: <b>DWORD</b>

This parameter is ignored.


### -param dwLen [in]

Type: <b>DWORD</b>

The size, in bytes, of the buffer pointed to by the <i>lpData</i> parameter. 

                    

Call the <a href="https://msdn.microsoft.com/e0e841b9-0014-4c7e-a4c7-0478960f962b">GetFileVersionInfoSizeEx</a> function first to determine the size, in bytes, of a file's version information. The <i>dwLen</i> parameter should be equal to or greater than that value.

If the buffer pointed to by <i>lpData</i> is not large enough, the function truncates the file's version information to the size of the buffer.


### -param lpData [out]

Type: <b>LPVOID</b>

When this function returns, contains a pointer to a buffer that contains the file-version information.


            You can use this value in a subsequent call to the <a href="https://msdn.microsoft.com/4fc3e2f0-0d9b-4974-b091-98908691bb14">VerQueryValue</a> function to retrieve data from the buffer.
          


#### - lptstrFilename [in]

Type: <b>LPCTSTR</b>

The name of the file. If a full path is not specified, the function uses the search sequence specified by the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> function.


## -returns



Type: <b>BOOL</b>


          If the function succeeds, the return value is nonzero.


            If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks




        Call the <a href="https://msdn.microsoft.com/e0e841b9-0014-4c7e-a4c7-0478960f962b">GetFileVersionInfoSizeEx</a> function before calling the <b>GetFileVersionInfoEx</b> function. To retrieve information from the file-version information buffer, use the <a href="https://msdn.microsoft.com/4fc3e2f0-0d9b-4974-b091-98908691bb14">VerQueryValue</a> function.
      




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/44679c26-f1ac-409c-8a25-abc5bfd888ac">GetFileVersionInfo</a>



<a href="https://msdn.microsoft.com/e0e841b9-0014-4c7e-a4c7-0478960f962b">GetFileVersionInfoSizeEx</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/7864510f-1894-4f17-bf7b-fd5bc1ba4aae">VS_VERSIONINFO</a>



<a href="https://msdn.microsoft.com/4fc3e2f0-0d9b-4974-b091-98908691bb14">VerQueryValue</a>



<a href="https://msdn.microsoft.com/60de7900-56b9-4481-bef9-b4079eedf926">Version Information</a>
 

 

