---
UID: NF:combaseapi.DllCanUnloadNow
title: DllCanUnloadNow function
author: windows-sdk-content
description: Determines whether the DLL that implements this function is in use. If not, the caller can unload the DLL from memory.
old-location: com\dllcanunloadnow.htm
tech.root: com
ms.assetid: a47df9eb-97cb-4875-a121-1dabe7bc9db6
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: DllCanUnloadNow, DllCanUnloadNow function [COM], _com_DllCanUnloadNow, com.dllcanunloadnow, combaseapi/DllCanUnloadNow
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: combaseapi.h
req.include-header: Objbase.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - combaseapi.h
api_name:
 - DllCanUnloadNow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DllCanUnloadNow function


## -description


Determines whether the DLL that implements this function is in use. If not, the caller can unload the DLL from memory.

OLE does not provide this function. DLLs that support the OLE Component Object Model (COM) should implement and export <b>DllCanUnloadNow</b>.


## -parameters






## -returns



If the function succeeds, the return value is S_OK. Otherwise, it is S_FALSE.




## -remarks



A call to <b>DllCanUnloadNow</b> determines whether the DLL from which it is exported is still in use. A DLL is no longer in use when it is not managing any existing objects (the reference count on all of its objects is 0). 



<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
You should not have to call <b>DllCanUnloadNow</b> directly. OLE calls it only through a call to the <a href="https://msdn.microsoft.com/188e9a3b-39cc-454e-af65-4ac797e275d4">CoFreeUnusedLibraries</a> function. When it returns S_OK, <b>CoFreeUnusedLibraries</b> frees the DLL.



<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
You must implement <b>DllCanUnloadNow</b> in, and export it from, DLLs that are to be dynamically loaded through a call to the <a href="https://msdn.microsoft.com/65e758ce-50a4-49e8-b3b2-0cd148d2781a">CoGetClassObject</a> function. (You also need to implement and export the <a href="https://msdn.microsoft.com/42c08149-c251-47f7-a81f-383975d7081c">DllGetClassObject</a> function in the same DLL).

If a DLL loaded through a call to <a href="https://msdn.microsoft.com/65e758ce-50a4-49e8-b3b2-0cd148d2781a">CoGetClassObject</a> fails to export <b>DllCanUnloadNow</b>, the DLL will not be unloaded until the application calls the <a href="https://msdn.microsoft.com/9411cbed-fa3b-46f7-b677-6ada53324edc">CoUninitialize</a> function to release the OLE libraries.

<b>DllCanUnloadNow</b> should return S_FALSE if there are any existing references to objects that the DLL manages.




## -see-also




<a href="https://msdn.microsoft.com/42c08149-c251-47f7-a81f-383975d7081c">DllGetClassObject</a>
 

 

