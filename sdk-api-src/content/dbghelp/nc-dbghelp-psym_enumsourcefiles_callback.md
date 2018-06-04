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

# PSYM_ENUMSOURCEFILES_CALLBACK callback function


## -description


An application-defined callback function used with the 
<a href="https://msdn.microsoft.com/4649bdc6-74c5-4529-bedc-64e0277144d0">SymEnumSourceFiles</a> function.

The <b>PSYM_ENUMSOURCEFILES_CALLBACK</b> and <b>PSYM_ENUMSOURCEFILES_CALLBACKW</b> types define a pointer to this callback function. 
<b>SymEnumSourceFilesProc</b> is a placeholder for the application-defined function name.


## -parameters




### -param pSourceFile [in]

A pointer to a 
<a href="https://msdn.microsoft.com/b41b844d-85d2-4ea3-bdd9-1564898da9e1">SOURCEFILE</a> structure that provides information about the source file.


### -param UserContext [in, optional]

The user-defined value passed from the 
<a href="https://msdn.microsoft.com/4649bdc6-74c5-4529-bedc-64e0277144d0">SymEnumSourceFiles</a> function, or <b>NULL</b>. This parameter is typically used by an application to pass a pointer to a data structure that provides context information for the callback function.


## -returns




						If the function returns <b>TRUE</b>, the enumeration will continue.
						

If the function returns <b>FALSE</b>, the enumeration will stop.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/b41b844d-85d2-4ea3-bdd9-1564898da9e1">SOURCEFILE</a>



<a href="https://msdn.microsoft.com/4649bdc6-74c5-4529-bedc-64e0277144d0">SymEnumSourceFiles</a>
 

 

