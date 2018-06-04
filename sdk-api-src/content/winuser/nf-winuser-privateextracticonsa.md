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

# PrivateExtractIconsA function


## -description


<p class="CCE_Message">[This function is not intended for general
      use. It may
      be altered or unavailable in subsequent versions of Windows.]

Creates an array of handles to icons that are extracted from a specified file.


## -parameters




### -param szFileName

TBD


### -param nIconIndex [in]

Type: <b>int</b>

The zero-based index of the first icon to extract. For example,
				  if this value is zero, the function extracts the first icon in the specified
				  file.


### -param cxIcon [in]

Type: <b>int</b>

The horizontal icon size wanted. See Remarks.


### -param cyIcon [in]

Type: <b>int</b>

The vertical icon size wanted. See Remarks.


### -param phicon [out, optional]

Type: <b>HICON*</b>

A pointer to the returned array of icon handles.


### -param piconid [out, optional]

Type: <b>UINT*</b>

A pointer to a returned resource identifier for the icon that best
				fits the current display device.  The returned identifier is 0xFFFFFFFF if the
				identifier is not available for this format.  The returned identifier is 0 if
				the identifier cannot otherwise be obtained.


### -param nIcons [in]

Type: <b>UINT</b>

The number of icons to extract from the file. This parameter
				is only valid when extracting from .exe and .dll files.


### -param flags [in]

Type: <b>UINT</b>

Specifies flags that control this function.  These flags are the LR_*
				flags used by the <a href="https://msdn.microsoft.com/27a18763-60e0-4a91-9262-807ea2b67416">LoadImage</a> function.


#### - lpszFile [in]

Type: <b>LPCTSTR</b>

The path and name of the file
				from which the icon(s) are to be extracted.


## -returns



Type: <b>UINT</b>

If the <i>phicon</i>
				parameter is <b>NULL</b> and this function succeeds, then the return
				value is the number of icons in the file.  If the function fails then the
				return value is 0.

If the <i>phicon</i> parameter is
        not <b>NULL</b> and the function succeeds, then the return value is the
        number of icons extracted.  Otherwise, the return value is 0xFFFFFFFF if the file
        is not found.




## -remarks



This function extracts from executable (.exe), DLL (.dll),
      icon (.ico), cursor (.cur), animated cursor (.ani), and bitmap (.bmp) files.
      Extractions from Windows 3.x 16-bit executables (.exe or .dll) are
      also supported.

The <i>cxIcon</i> and
      <i>cyIcon</i> parameters specify the
      size of the icons to extract.  Two sizes can be extracted by putting the
      first size in the LOWORD of the parameter and the second size in the HIWORD.
      For example, <code>MAKELONG(24, 48)</code> for both the cxIcon and cyIcon parameters would extract
      both 24 and 48 size icons.

You must destroy all icons extracted by <b>PrivateExtractIcons</b>
			by calling the <a href="https://msdn.microsoft.com/ffe21e34-ebe0-4ec8-830f-64c733ef9097">DestroyIcon</a> function. 

This function was not included in the SDK headers and libraries until Windows XP Service Pack 1 (SP1) and Windows Server 2003. If you do not have a header file and import library for this function, you can call the function using <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a>.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/ffe21e34-ebe0-4ec8-830f-64c733ef9097">DestroyIcon</a>



<a href="https://msdn.microsoft.com/323c5e09-4e22-4a67-b8aa-5e5f369fb585">ExtractIcon</a>



<a href="https://msdn.microsoft.com/ef7a141f-9711-4345-8035-b7ad18a37caf">ExtractIconEx</a>



<a href="https://msdn.microsoft.com/1dc588f4-b032-40a8-82ef-5b9fc04abb0b">Icons</a>



<b>Reference</b>
 

 

