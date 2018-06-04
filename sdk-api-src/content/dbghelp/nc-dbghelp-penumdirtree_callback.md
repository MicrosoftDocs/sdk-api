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

# PENUMDIRTREE_CALLBACK callback function


## -description


An application-defined callback function used with the 
<a href="https://msdn.microsoft.com/2dd132f3-83d4-4afd-b44d-9f8d385d6116">EnumDirTree</a> function. It is called every time a match is found.

The <b>PENUMDIRTREE_CALLBACK</b> and <b>PENUMDIRTREE_CALLBACKW</b> types define a pointer to this callback function. 
<i>EnumDirTreeProc</i> is a placeholder for the application-defined function name.


## -parameters




### -param FilePath [in]

A pointer to a buffer that receives the full path of the file that is found.


### -param CallerData [in, optional]

A user-defined value specified in 
<a href="https://msdn.microsoft.com/2dd132f3-83d4-4afd-b44d-9f8d385d6116">EnumDirTree</a>, or <b>NULL</b>. Typically, this parameter is used by an application to pass a pointer to a data structure that enables the callback function to establish some context.


## -returns



To continue enumeration, the callback function must return <b>FALSE</b>.

To stop enumeration, the callback function must return <b>TRUE</b>.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/2dd132f3-83d4-4afd-b44d-9f8d385d6116">EnumDirTree</a>
 

 

