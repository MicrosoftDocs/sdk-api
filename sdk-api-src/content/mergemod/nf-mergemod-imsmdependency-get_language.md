---
UID: NF:mergemod.IMsmDependency.get_Language
title: IMsmDependency::get_Language
author: windows-sdk-content
description: The get_Language method retrieves the Language property of the Dependency object. This method returns the LANGID of the required module.
old-location: setup\imsmdependency_get_language.htm
tech.root: msi
ms.assetid: eb7e224d-948e-46d6-ac1b-cd851530cc8b
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IMsmDependency interface,get_Language method, IMsmDependency.get_Language, IMsmDependency::get_Language, _msi_get_language_function_dependency_object_, get_Language, get_Language method, get_Language method,IMsmDependency interface, mergemod/IMsmDependency::get_Language, setup.imsmdependency_get_language
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
 - IMsmDependency.get_Language
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMsmDependency::get_Language


## -description


The 
<b>get_Language</b> method retrieves the 
<a href="https://msdn.microsoft.com/9b0608d1-b6e8-4cf9-8119-3c2909156516">Language</a> property of the 
<a href="https://msdn.microsoft.com/3157f07d-99de-4628-9b03-eb86eb4896a4">Dependency</a> object. This method returns the <b>LANGID</b> of the required module.


## -parameters




### -param Language [out]

A pointer to a location in memory that receives the language.


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
Language is null.

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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/517cf174-418a-4717-a25f-1736225016a1">IMsmDependency</a>



<a href="https://msdn.microsoft.com/877d3691-948f-4aea-89d8-0ff008126ccc">Merge Module Automation</a>
 

 

