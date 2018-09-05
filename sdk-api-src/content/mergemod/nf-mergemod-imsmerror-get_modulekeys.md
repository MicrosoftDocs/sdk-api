---
UID: NF:mergemod.IMsmError.get_ModuleKeys
title: IMsmError::get_ModuleKeys
author: windows-sdk-content
description: The read-only ModuleKeys property of the Error object returns a pointer to a string collection containing the primary keys of the row in the module causing the error, one key per entry in the collection.
old-location: setup\error_modulekeys.htm
old-project: msi
ms.assetid: b02b609b-4682-4228-b29a-364f079e863c
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: Error object,ModuleKeys property, Error.ModuleKeys, IMsmError.get_ModuleKeys, IMsmError::get_ModuleKeys, ModuleKeys property, ModuleKeys property,Error object, _msi_modulekeys_property, get_ModuleKeys, setup.error_modulekeys
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
 - Error.ModuleKeys
 - IMsmError.get_ModuleKeys
product: Windows
targetos: Windows
req.lib: 
req.dll: Mergemod.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMsmError::get_ModuleKeys


## -description


The read-only 
<b>ModuleKeys</b> property of the 
<a href="https://msdn.microsoft.com/38025e21-2d31-40f8-a088-2d3912c2893e">Error</a> object returns a pointer to a string collection containing the primary keys of the row in the module causing the error, one key per entry in the collection.

This property is read-only.


## -parameters


## -remarks



The client is responsible for releasing the string collection when it is no longer needed.

The collection is empty if the values do not apply to the type of the error. You can determine the type of error by calling the 
<a href="https://msdn.microsoft.com/5567ba71-c815-4434-962c-aa46cd171712">Type</a> property of the 
<a href="https://msdn.microsoft.com/38025e21-2d31-40f8-a088-2d3912c2893e">Error</a> object.

<h3><a id="C__"></a><a id="c__"></a>C++</h3>
See 
<a href="https://msdn.microsoft.com/f2f483c7-8d38-416e-af92-fd7ab6aef459">get_ModuleKeys</a> function.



