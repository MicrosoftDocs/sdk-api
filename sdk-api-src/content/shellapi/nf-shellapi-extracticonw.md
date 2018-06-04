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

# ExtractIconW function


## -description


Retrieves a handle to an icon from the specified executable file, DLL, or icon file.

To retrieve an array of handles to large or small icons, use the <a href="https://msdn.microsoft.com/ef7a141f-9711-4345-8035-b7ad18a37caf">ExtractIconEx</a> function.


## -parameters




### -param hInst

Type: <b>HINSTANCE</b>

A handle to the instance of the application calling the function. 


### -param pszExeFileName

TBD


### -param nIconIndex [in]

Type: <b>UINT</b>

The zero-based index of the icon to retrieve. For example, if this value is 0, the function returns a handle to the first icon in the specified file.

If this value is -1, the function returns the total number of icons in the specified file. If the file is an executable file or DLL, the return value is the number of <b>RT_GROUP_ICON</b> resources. If the file is an .ICO file, the return value is 1. 

 If this value is a negative number not equal to –1, the function returns a handle to the icon in the specified file whose resource identifier is equal to the absolute value of <i>nIconIndex</i>. For example, you should use –3 to extract the icon whose resource identifier is 3. To extract the icon whose resource identifier is 1, use the <a href="https://msdn.microsoft.com/ef7a141f-9711-4345-8035-b7ad18a37caf">ExtractIconEx</a> function. 


#### - lpszExeFileName [in]

Type: <b>LPCTSTR</b>

The name of an executable file, DLL, or icon file. 


## -returns



Type: <b>HICON</b>

The return value is a handle to an icon. If the file specified was not an executable file, DLL, or icon file, the return is 1. If no icons were found in the file, the return value is <b>NULL</b>.




## -remarks



You must destroy the icon handle returned by <b>ExtractIcon</b> by calling the <a href="https://msdn.microsoft.com/ffe21e34-ebe0-4ec8-830f-64c733ef9097">DestroyIcon</a> function. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/ffe21e34-ebe0-4ec8-830f-64c733ef9097">DestroyIcon</a>



<a href="https://msdn.microsoft.com/1dc588f4-b032-40a8-82ef-5b9fc04abb0b">Icons</a>



<b>Reference</b>
 

 

