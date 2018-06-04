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

# BeginUpdateResourceA function


## -description


Retrieves a handle that can be used by the <a href="https://msdn.microsoft.com/2984d87c-1cc4-4d4b-8542-c8aeb3b9d40e">UpdateResource</a> function to add, delete, or replace resources in a binary module.


## -parameters




### -param pFileName [in]

Type: <b>LPCTSTR</b>

The binary file in which to update resources. An application must be able to obtain write-access to this file; the file referenced by <i>pFileName</i> cannot be currently executing. If <i>pFileName</i> does not specify a full path, the system searches for the file in the current directory. 


### -param bDeleteExistingResources [in]

Type: <b>BOOL</b>

Indicates whether to delete the <i>pFileName</i> parameter's existing resources. If this parameter is <b>TRUE</b>, existing resources are deleted and the updated file includes only resources added with the <a href="https://msdn.microsoft.com/2984d87c-1cc4-4d4b-8542-c8aeb3b9d40e">UpdateResource</a> function. If this parameter is <b>FALSE</b>, the updated file includes existing resources unless they are explicitly deleted or replaced by using <b>UpdateResource</b>. 


## -returns



Type: <b>HANDLE</b>

If the function succeeds, the return value is a handle that can be used by the <a href="https://msdn.microsoft.com/2984d87c-1cc4-4d4b-8542-c8aeb3b9d40e">UpdateResource</a> and <a href="https://msdn.microsoft.com/19d251ec-ee98-4455-a091-e2e4a3b80092">EndUpdateResource</a> functions. The return value is <b>NULL</b> if the specified file is not a PE, the file does not exist, or the file cannot be opened for writing. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



It is recommended that the resource file is not loaded before this function is called. However, if that file is already loaded, it will not cause an error to be returned.

There are some restrictions on resource updates in files that contain  Resource Configuration(RC Config) data: LN files and the associated .mui files. Details on which types of resources are allowed to be updated in these files are in the Remarks section for the <a href="https://msdn.microsoft.com/2984d87c-1cc4-4d4b-8542-c8aeb3b9d40e">UpdateResource</a> function.

This function can update resources within modules that contain both code and resources. As noted above, there are restrictions on resource updates in LN files and .mui files, both of which contain RC Config data; details of the restrictions are in the reference for the <a href="https://msdn.microsoft.com/2984d87c-1cc4-4d4b-8542-c8aeb3b9d40e">UpdateResource</a> function.
			


#### Examples

For an example see, <a href="using_resources.htm">Updating Resources</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/19d251ec-ee98-4455-a091-e2e4a3b80092">EndUpdateResource</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/ff321356-c999-4021-a537-fbe863996e24">Resources</a>



<a href="https://msdn.microsoft.com/2984d87c-1cc4-4d4b-8542-c8aeb3b9d40e">UpdateResource</a>
 

 

