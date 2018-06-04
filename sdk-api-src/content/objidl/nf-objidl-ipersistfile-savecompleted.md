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

# IPersistFile::SaveCompleted


## -description


Notifies the object that it can write to its file. It does this by notifying the object that it can revert from NoScribble mode (in which it must not write to its file), to Normal mode (in which it can). The component enters NoScribble mode when it receives an <a href="https://msdn.microsoft.com/da9581e8-98c7-4592-8ee1-a1bc8232635b">IPersistFile::Save</a> call.


## -parameters




### -param pszFileName [in]

The absolute path of the file where the object was saved previously.


## -returns



This method always returns S_OK.




## -remarks



<b>SaveCompleted</b> is called when a call to <a href="https://msdn.microsoft.com/da9581e8-98c7-4592-8ee1-a1bc8232635b">IPersistFile::Save</a> is completed, and the file that was saved is now the current working file (having been saved with <b>Save</b> or <b>Save As</b> operations). The call to <b>Save</b> puts the object into NoScribble mode so it cannot write to its file. When <b>SaveCompleted</b> is called, the object reverts to Normal mode, in which it is free to write to its file.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
OLE does not call the <b>SaveCompleted</b> method. Typically, applications would not call it unless they are saving objects directly to files, an operation which is generally left to the end-user.





## -see-also




<a href="https://msdn.microsoft.com/7d34507f-8a16-43b4-8225-010798abc546">IPersistFile</a>
 

 

