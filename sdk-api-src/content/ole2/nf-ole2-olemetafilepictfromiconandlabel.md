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

# OleMetafilePictFromIconAndLabel function


## -description


Creates a metafile in which the specified icon and label are drawn.


## -parameters




### -param hIcon [in]

Handle to the icon that is to be drawn into the metafile. This parameter can be <b>NULL</b>. If <i>hIcon</i> is <b>NULL</b>, this function returns <b>NULL</b> without creating a metafile.


### -param lpszLabel [in]

The icon label. This parameter can be <b>NULL</b>. If <i>lpszLabel</i> is <b>NULL</b>, the resulting metafile will not include a label. 


### -param lpszSourceFile [in]

The path and file name of the icon file. This string can be obtained through the user interface or from the registration database. This parameter can be <b>NULL</b>.


### -param iIconIndex [in]

The location of the icon within the file named by <i>lpszSourceFile</i>, expressed as an offset in bytes from the beginning of file.


## -returns



A global handle to a <a href="_win32_METAFILEPICT_str_cpp">METAFILEPICT</a> structure containing the icon and label. The metafile uses the MM_ANISOTROPIC mapping mode.

If an error occurs, the returned handle is <b>NULL</b>. In this case, the caller can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> to obtain further information. 





## -remarks



This function is called by <a href="https://msdn.microsoft.com/2fa9cd75-4dc6-45a3-aa62-e82bd28289a5">OleGetIconOfFile</a> and <a href="https://msdn.microsoft.com/88ac1c14-b5a8-4100-9fa5-d7af35052b48">OleGetIconOfClass</a>.

If <i>lpszSourceFile</i> is not <b>NULL</b> and <i>iIconIndex</i> is not 0, the name of the source file passed in <i>lpszSourceFile</i> and the index passed by <i>iIconIndex</i> are added to the created metafile as a comment record.




## -see-also




<a href="https://msdn.microsoft.com/88ac1c14-b5a8-4100-9fa5-d7af35052b48">OleGetIconOfClass</a>



<a href="https://msdn.microsoft.com/2fa9cd75-4dc6-45a3-aa62-e82bd28289a5">OleGetIconOfFile</a>
 

 

