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

# ExtractAssociatedIconW function


## -description


Retrieves a handle to an indexed icon found in a file or an icon found in an associated executable file. 


## -parameters




### -param hInst

Type: <b>HINSTANCE</b>

A handle to the instance of the application calling the function. 


### -param pszIconPath

TBD


### -param piIcon

TBD




#### - lpIconPath [in, out]

Type: <b>LPTSTR</b>

The full path and file name of the file that contains the icon. The function extracts the icon handle from that file, or from an executable file associated with that file. If the icon handle is obtained from an executable file, the function stores the full path and file name of that executable in the string pointed to by <i>lpIconPath</i>. 


#### - lpiIcon [in, out]

Type: <b>WORD*</b>

The index of the icon whose handle is to be obtained. If the icon handle is obtained from an executable file, the function stores the icon's identifier in this parameter. 


## -returns



Type: <b>HICON</b>

If the function succeeds, the return value is an icon handle. If the icon is extracted from an associated executable file, the function stores the full path and file name of the executable file in the string pointed to by <i>lpIconPath</i>, and stores the icon's identifier in the variable pointed to by <i>lpiIcon</i>.

If the function fails, the return value is <b>NULL</b>.




## -remarks



You must destroy the icon handle returned by <b>ExtractAssociatedIcon</b> by calling the <a href="https://msdn.microsoft.com/ffe21e34-ebe0-4ec8-830f-64c733ef9097">DestroyIcon</a> function. 

The <b>ExtractAssociatedIcon</b> function first looks for the indexed icon in the file specified by <i>lpIconPath</i>. If the function cannot obtain the icon handle from that file, and the file has an associated executable file, it looks in that executable file for an icon. Associations with executable files are based on file name extensions, are stored in the per-user part of the registry, and can be defined using File Manager's Associate command. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/323c5e09-4e22-4a67-b8aa-5e5f369fb585">ExtractIcon</a>



<a href="https://msdn.microsoft.com/1dc588f4-b032-40a8-82ef-5b9fc04abb0b">Icons</a>



<b>Reference</b>
 

 

