---
UID: NF:mergemod.IMsmError.get_Path
title: IMsmError::get_Path
author: windows-sdk-content
description: In Windows Installer versions 1.0 and 1.1 the Path property is always the empty string. Future versions may use this value to return the path to the file or directory that could not be created.
old-location: setup\error_path.htm
old-project: msi
ms.assetid: b79dd347-acda-47d7-aa3b-c0f9a6ca1d3b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: Error object,Path property, Error.Path, IMsmError.get_Path, IMsmError::get_Path, Path property, Path property,Error object, _msi_path_property, get_Path, setup.error_path
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mergemod.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Mergemod.dll 1.0 or later
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
tech.root: 
req.typenames: WIN32_MEMORY_REGION_INFORMATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mergemod.dll
api_name:
 - Error.Path
 - IMsmError.get_Path
product: Windows
targetos: Windows
req.lib: 
req.dll: Mergemod.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMsmError::get_Path


## -description


In Windows Installer versions 1.0 and 1.1 the 
<b>Path</b> property is always the empty string. Future versions may use this value to return the path to the file or directory that could not be created.

This property is read-only.


## -parameters


## -remarks



This value is only valid for errors of type msmErrorFileCreate or msmErrorDirCreate. You can determine the type of error by calling 
<a href="https://msdn.microsoft.com/5567ba71-c815-4434-962c-aa46cd171712">Type</a> property of the 
<a href="https://msdn.microsoft.com/38025e21-2d31-40f8-a088-2d3912c2893e">Error</a> object.

<h3><a id="C__"></a><a id="c__"></a>C++</h3>
See 
<a href="https://msdn.microsoft.com/a431f0c6-6551-4983-8638-0a76cada822d">get_Path</a> function.



