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

# PENUMSOURCEFILETOKENSCALLBACK callback function


## -description


An application-defined callback function used with the 
<a href="https://msdn.microsoft.com/0377ef07-bf9f-4938-8fc4-ae14373db590">SymEnumSourceFileTokens</a> function which enumerates the <a href="https://msdn.microsoft.com/c7bf51ce-7fb4-49aa-ad33-e551b2c8362b">source server</a> version control information stored in the PDB for a module.

The <b>PENUMSOURCEFILETOKENSCALLBACK</b> type defines a pointer to this callback function. 
<b>SymEnumSourceFileTokensProc</b> is a placeholder for the application-defined function name.


## -parameters




### -param token [in]

A pointer to an opaque data structure that contains the version control information corresponding to a particular individual source file.     The usage of this token is detailed below.


### -param size [in]

The size of the data in the <i>token</i> parameter.


## -returns




						If the function returns <b>TRUE</b>, the enumeration will continue.
						

If the function returns <b>FALSE</b>, the enumeration will stop.




## -remarks



An application can use this token to extract a source file from version control by calling <a href="https://msdn.microsoft.com/67a282c2-99f8-4e35-9323-a81327404d1a">SymGetSourceFileFromToken</a>.  

To get individual variables from the token, call <a href="https://msdn.microsoft.com/05e9005a-aef3-44a3-a73b-21830799a3d5">SymGetSourceVarFromToken</a>.  The names of the variables differ based on the scripts used to create the tokens.  See <a href="https://msdn.microsoft.com/c7bf51ce-7fb4-49aa-ad33-e551b2c8362b">Source Server</a> for details.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/c7bf51ce-7fb4-49aa-ad33-e551b2c8362b">Source Server</a>



<a href="https://msdn.microsoft.com/0377ef07-bf9f-4938-8fc4-ae14373db590">SymEnumSourceFileTokens</a>



<a href="https://msdn.microsoft.com/1d2115fb-2725-4fae-abb7-ff1b8a802c69">SymGetSourceFile</a>



<a href="https://msdn.microsoft.com/67a282c2-99f8-4e35-9323-a81327404d1a">SymGetSourceFileFromToken</a>
 

 

