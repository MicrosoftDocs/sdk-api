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

# GetFileVersionInfoSizeExA function


## -description


Determines whether the operating system can retrieve version information for a specified file. If version information is available, <b>GetFileVersionInfoSizeEx</b> returns the size, in bytes, of that information.


## -parameters




### -param dwFlags [in]

Type: <b>DWORD</b>

Controls which MUI DLLs (if any) from which the version resource is extracted. Zero or more of the following flags.

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
<dt>0x002</dt>
</dl>
</td>
<td width="60%">
Loads the version resource strings from the corresponding MUI file, if available, and loads the binary version information (<b>VS_FIXEDFILEINFO</b>) from the corresponding language-neutral file, if available. 

</td>
</tr>
</table>
 


### -param lpwstrFilename

TBD


### -param lpdwHandle [out]

Type: <b>LPDWORD</b>

When this function returns, contains a pointer to a variable that is set to zero because this function sets it to zero. This parameter exists for historical reasons.


#### - lptstrFilename [in]

Type: <b>LPCTSTR</b>

The name of the file of interest. The function uses the search sequence specified by the  <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> function.


## -returns



Type: <b>DWORD</b>

If the function succeeds, the return value is the size, in bytes, of the file's version information.
                    
                    

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Call the <b>GetFileVersionInfoSizeEx</b> function before calling the <a href="https://msdn.microsoft.com/beeab559-e093-443c-bca2-a81b2e396beb">GetFileVersionInfoEx</a> function. The size returned by <b>GetFileVersionInfoSizeEx</b> indicates the buffer size required for the version information returned by <b>GetFileVersionInfoEx</b>.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/beeab559-e093-443c-bca2-a81b2e396beb">GetFileVersionInfoEx</a>



<a href="https://msdn.microsoft.com/e2903940-a775-4bbc-bf52-6660f18a4d72">GetFileVersionInfoSize</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/7864510f-1894-4f17-bf7b-fd5bc1ba4aae">VS_VERSIONINFO</a>



<a href="https://msdn.microsoft.com/4fc3e2f0-0d9b-4974-b091-98908691bb14">VerQueryValue</a>



<a href="https://msdn.microsoft.com/60de7900-56b9-4481-bef9-b4079eedf926">Version Information</a>
 

 

