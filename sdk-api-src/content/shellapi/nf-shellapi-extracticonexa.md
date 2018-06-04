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

# ExtractIconExA function


## -description


Creates an array of handles to large or small icons extracted from the specified executable file, DLL, or icon file. 


## -parameters




### -param lpszFile [in]

Type: <b>LPCTSTR</b>

The name of an executable file, DLL, or icon file from which icons will be extracted. 


### -param nIconIndex [in]

Type: <b>int</b>

The zero-based index of the first icon to extract. For example, if this value is zero, the function extracts the first icon in the specified file. 

If this value is –1 and <i>phiconLarge</i> and <i>phiconSmall</i> are both <b>NULL</b>, the function returns the total number of icons in the specified file. If the file is an executable file or DLL, the return value is the number of <b>RT_GROUP_ICON</b> resources. If the file is an .ico file, the return value is 1. 


						 If this value is a negative number and either <i>phiconLarge</i> or <i>phiconSmall</i> is not <b>NULL</b>, the function begins by extracting the icon whose resource identifier is equal to the absolute value of <i>nIconIndex</i>. For example, use -3 to extract the icon whose resource identifier is 3. 


### -param phiconLarge [out, optional]

Type: <b>HICON*</b>

An array of icon handles that receives handles to the large icons extracted from the file. If this parameter is <b>NULL</b>, no large icons are extracted from the file. 


### -param phiconSmall [out, optional]

Type: <b>HICON*</b>

An array of icon handles that receives handles to the small icons extracted from the file. If this parameter is <b>NULL</b>, no small icons are extracted from the file. 


### -param nIcons [in]

Type: <b>UINT</b>

The number of icons to be extracted from the file. 


## -returns



Type: <b>UINT</b>

If the <i>nIconIndex</i> parameter is -1, the <i>phiconLarge</i> parameter is <b>NULL</b>, and the <i>phiconSmall</i> parameter is <b>NULL</b>, then the return value is the number of icons contained in the specified file. Otherwise, the return value is the number of icons successfully extracted from the file. 




## -remarks



You must destroy all icons extracted by <b>ExtractIconEx</b> by calling the <a href="https://msdn.microsoft.com/ffe21e34-ebe0-4ec8-830f-64c733ef9097">DestroyIcon</a> function. 

To retrieve the dimensions of the large and small icons, use the <a href="https://msdn.microsoft.com/d063857b-6036-4e68-80af-9c70d12ae29e">GetSystemMetrics</a> function with the <b>SM_CXICON</b>, <b>SM_CYICON</b>, <b>SM_CXSMICON</b>, and <b>SM_CYSMICON</b> flags.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/ffe21e34-ebe0-4ec8-830f-64c733ef9097">DestroyIcon</a>



<a href="https://msdn.microsoft.com/323c5e09-4e22-4a67-b8aa-5e5f369fb585">ExtractIcon</a>



<a href="https://msdn.microsoft.com/1dc588f4-b032-40a8-82ef-5b9fc04abb0b">Icons</a>



<b>Reference</b>
 

 

