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

# SHLoadInProc function


## -description


Creates an instance of the specified object class from within the context of the Shell's process.
        
            

<b>Windows Vista</b> and later: This function has been disabled and returns E_NOTIMPL.


## -parameters




### -param rclsid [in]

Type: <b>REFCLSID</b>

The CLSID of the object class to be created.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise. In Windows Vista and later versions, always returns E_NOTIMPL.




## -remarks



<div class="alert"><b>Note</b>  This function is available through Windows XP Service Pack 2 (SP2) and Windows Server 2003. It is not available in later versions of Windows, including Windows Vista.</div>
<div> </div>
This function creates the requested object instance by calling the <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a> function and immediately releasing the returned object. The associated DLL is unloaded according to standard Component Object Model (COM) rules when it returns S_OK from its <a href="https://msdn.microsoft.com/a47df9eb-97cb-4875-a121-1dabe7bc9db6">DllCanUnloadNow</a> function.



