---
UID: NF:mergemod.IMsmGetFiles.get_ModuleFiles
title: IMsmGetFiles::get_ModuleFiles
author: windows-sdk-content
description: The get_ModuleFiles method retrieves the ModuleFiles property of the GetFiles object.
old-location: setup\imsmgetfiles_get_modulefiles.htm
tech.root: msi
ms.assetid: 525c1a30-a870-4303-b704-e8b37f9e641f
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IMsmGetFiles interface,get_ModuleFiles method, IMsmGetFiles.get_ModuleFiles, IMsmGetFiles::get_ModuleFiles, _msi_get_modulefiles_function, get_ModuleFiles, get_ModuleFiles method, get_ModuleFiles method,IMsmGetFiles interface, mergemod/IMsmGetFiles::get_ModuleFiles, setup.imsmgetfiles_get_modulefiles
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mergemod.h
req.include-header: 
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
req.lib: 
req.dll: Mergemod.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mergemod.dll
api_name:
 - IMsmGetFiles.get_ModuleFiles
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMsmGetFiles::get_ModuleFiles


## -description


The 
<b>get_ModuleFiles</b> method retrieves the 
<a href="https://msdn.microsoft.com/e1c8049c-b271-4def-abde-89ea99393574">ModuleFiles</a> property of the 
<a href="https://msdn.microsoft.com/f3bf64ec-75f7-43a6-bbd8-a51508c57002">GetFiles</a> object. This method returns the primary keys in the 
<a href="https://msdn.microsoft.com/31d0e727-a9eb-4cd2-a211-ea7b138d0173">File table</a> of the currently open module. The primary keys are returned as a collection of strings. The module must be opened by a call to the 
<a href="https://msdn.microsoft.com/37225e61-c24f-4a44-8fdf-673590a6e09d">OpenModule</a> function before calling 
<b>get_ModuleFiles</b>.


## -parameters




### -param Files [out]

Collection of IMsmStrings that are the primary keys of the 
<a href="https://msdn.microsoft.com/31d0e727-a9eb-4cd2-a211-ea7b138d0173">File table</a> for the currently open module.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
No module is open.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FUNCTION_FAILED as HRESULT</b></dt>
</dl>
</td>
<td width="60%">
The function failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE as HRESULT</b></dt>
</dl>
</td>
<td width="60%">
The function failed.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/877d3691-948f-4aea-89d8-0ff008126ccc">Merge Module Automation</a>
 

 

