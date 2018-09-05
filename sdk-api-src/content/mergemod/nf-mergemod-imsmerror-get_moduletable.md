---
UID: NF:mergemod.IMsmError.get_ModuleTable
title: IMsmError::get_ModuleTable
author: windows-sdk-content
description: The read-only ModuleTable Property returns the name of the table in the module that caused the error.
old-location: setup\error_moduletable.htm
old-project: msi
ms.assetid: 390f5889-d638-4c1c-b95c-76d38c934e7c
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: Error object,ModuleTable property, Error.ModuleTable, IMsmError.get_ModuleTable, IMsmError::get_ModuleTable, ModuleTable property, ModuleTable property,Error object, _msi_moduletable_property, get_ModuleTable, setup.error_moduletable
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
 - Error.ModuleTable
 - IMsmError.get_ModuleTable
product: Windows
targetos: Windows
req.lib: 
req.dll: Mergemod.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMsmError::get_ModuleTable


## -description


The read-only 
<b>ModuleTable</b> Property returns the name of the table in the module that caused the error.

This property is read-only.


## -parameters


## -remarks



The collection is empty if the values do not apply to the type of the error. You can determine the type of error by calling the 
<a href="https://msdn.microsoft.com/5567ba71-c815-4434-962c-aa46cd171712">Type</a> property of the 
<a href="https://msdn.microsoft.com/38025e21-2d31-40f8-a088-2d3912c2893e">Error</a> object.

<h3><a id="C__"></a><a id="c__"></a>C++</h3>
See 
<a href="https://msdn.microsoft.com/c24145dc-0907-4916-bbec-f9e0ec7584db">get_ModuleTable</a> function.



