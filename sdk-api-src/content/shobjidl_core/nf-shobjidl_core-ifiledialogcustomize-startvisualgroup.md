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

# IFileDialogCustomize::StartVisualGroup


## -description


Declares a visual group in the dialog. Subsequent calls to any "add" method add those elements to this group.


## -parameters




### -param dwIDCtl [in]

Type: <b>DWORD</b>


                  The ID of the visual group.
                


### -param pszLabel [in]

Type: <b>LPCWSTR</b>


                  A pointer to a buffer that contains text, as a null-terminated Unicode string, that appears next to the visual group.
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




                Controls will continue to be added to this visual group until you call <a href="https://msdn.microsoft.com/84aef9e1-2b70-4e8b-b261-cc49f8e65ead">IFileDialogCustomize::EndVisualGroup</a>.
              

A visual group can be hidden and disabled like any other control, except that doing so affects all of the controls within it. Individual members of the visual group can also be hidden and disabled singly.



