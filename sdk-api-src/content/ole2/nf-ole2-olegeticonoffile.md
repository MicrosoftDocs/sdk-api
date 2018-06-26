---
UID: NF:ole2.OleGetIconOfFile
title: OleGetIconOfFile function
author: windows-sdk-content
description: Returns a handle to a metafile containing an icon and string label for the specified file name.
old-location: com\olegeticonoffile.htm
old-project: com
ms.assetid: 2fa9cd75-4dc6-45a3-aa62-e82bd28289a5
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: OleGetIconOfFile, OleGetIconOfFile function [COM], _com_OleGetIconOfFile, com.olegeticonoffile, ole2/OleGetIconOfFile
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ole2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: QACONTROL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
api_name:
 - OleGetIconOfFile
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
req.product: ADAM
---

# OleGetIconOfFile function


## -description


Returns a handle to a metafile containing an icon and string label for the specified file name.


## -parameters




### -param lpszPath [in]

A pointer to a file for which the icon and string are to be requested.


### -param fUseFileAsLabel [in]

Indicates whether to use the file name as the icon label.


## -returns



If the function succeeds, the return value is a handle to a metafile that contains and icon and label for the specified file. If there is no CLSID in the registration database for the file, then the function returns the string "Document". If <i>lpszPath</i> is <b>NULL</b>, the function returns <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/88ac1c14-b5a8-4100-9fa5-d7af35052b48">OleGetIconOfClass</a>



<a href="https://msdn.microsoft.com/627a79eb-46dd-4df7-a0d6-cab37b73387a">OleMetafilePictFromIconAndLabel</a>
 

 

