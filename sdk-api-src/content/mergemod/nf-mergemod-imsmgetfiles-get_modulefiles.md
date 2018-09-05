---
UID: NF:mergemod.IMsmGetFiles.get_ModuleFiles
title: IMsmGetFiles::get_ModuleFiles
author: windows-sdk-content
description: ModuleFiles property of the GetFiles object returns all the primary keys of the File table for the currently open module.
old-location: setup\getfiles_modulefiles.htm
old-project: msi
ms.assetid: e1c8049c-b271-4def-abde-89ea99393574
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetFiles object,ModuleFiles property, GetFiles.ModuleFiles, IMsmGetFiles.get_ModuleFiles, IMsmGetFiles::get_ModuleFiles, ModuleFiles property, ModuleFiles property,GetFiles object, _msi_modulefiles_property, get_ModuleFiles, setup.getfiles_modulefiles
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
 - GetFiles.ModuleFiles
 - IMsmGetFiles.get_ModuleFiles
product: Windows
targetos: Windows
req.lib: 
req.dll: Mergemod.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMsmGetFiles::get_ModuleFiles


## -description


<b>ModuleFiles</b> property of the 
<a href="https://msdn.microsoft.com/f3bf64ec-75f7-43a6-bbd8-a51508c57002">GetFiles</a> object returns all the primary keys of the 
<a href="https://msdn.microsoft.com/31d0e727-a9eb-4cd2-a211-ea7b138d0173">File table</a> for the currently open module. The primary keys are returned as a collection of strings. The module must be opened by a call to the 
<a href="https://msdn.microsoft.com/fc976899-2c39-4314-b2fb-417e0dfc53b9">OpenModule</a> method of the 
<a href="https://msdn.microsoft.com/3f76ee8a-d195-4a69-99a3-31ef2c1c72d5">Merge object</a> before calling 
<b>ModuleFiles</b>.

This property is read-only.


## -parameters


## -remarks



Note that order of the files listed in the collection may not be in the same sequence as listed in the File table.

If the module has no File table, or contains no files in the particular language, ModuleFiles returns an empty collection of strings.

<h3><a id="C__"></a><a id="c__"></a>C++</h3>
See 
<a href="https://msdn.microsoft.com/525c1a30-a870-4303-b704-e8b37f9e641f">get_ModuleFiles</a> function.



