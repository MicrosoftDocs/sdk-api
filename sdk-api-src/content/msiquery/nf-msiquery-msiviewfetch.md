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

# MsiViewFetch function


## -description


The 
<b>MsiViewFetch</b> function fetches the next sequential record from the view. This function returns a handle that should be closed using 
<a href="https://msdn.microsoft.com/b9e90ed4-fda8-4628-a713-67c651e1b572">MsiCloseHandle</a>.


## -parameters




### -param hView [in]

Handle to the view to fetch from.


### -param phRecord [out]

Pointer to the handle for the fetched record.


## -returns



Note that in low memory situations, this function can raise a STATUS_NO_MEMORY exception.




## -remarks



If the 
<b>MsiViewFetch</b> function returns ERROR_FUNCTION_FAILED, it is possible that the 
<a href="https://msdn.microsoft.com/12b2373f-425a-4035-bdb4-be1a5469f1d7">MsiViewExecute</a> function was not called first. If more rows are available in the result set, 
<b>MsiViewFetch</b> returns <i>phRecord</i> as a handle to a record containing the requested column data, or <i>phRecord</i> is 0. For maximum performance, the same record should be used for all retrievals, or the record should be released by going out of scope.

Note that it is recommended to use variables of type PMSIHANDLE because the installer closes PMSIHANDLE objects as they go out of scope, whereas you must close MSIHANDLE objects by calling 
<a href="https://msdn.microsoft.com/b9e90ed4-fda8-4628-a713-67c651e1b572">MsiCloseHandle</a>. For more information see <a href="windows_installer_best_practices.htm">Use PMSIHANDLE instead of HANDLE</a> section in the <a href="https://msdn.microsoft.com/ff48d995-fe6f-4d1b-898d-67574ed3c5b7">Windows Installer Best Practices</a>.




## -see-also




<a href="database_functions.htm">General Database Access Functions</a>



<a href="https://msdn.microsoft.com/1b8fd935-4964-4875-801b-cc6765b16924">Working with Queries</a>
 

 

