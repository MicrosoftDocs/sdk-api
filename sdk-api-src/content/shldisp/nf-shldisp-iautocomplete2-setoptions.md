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

# IAutoComplete2::SetOptions


## -description


Sets the current autocomplete options.


## -parameters




### -param dwFlag [in]

Type: <b>DWORD</b>

One or more flags from the <a href="https://msdn.microsoft.com/e0a583da-c2bd-4757-868d-a63e697142e2">AUTOCOMPLETEOPTIONS</a> enumeration that specify autocomplete options.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The TAB key is disabled by default because it is typically used to navigate from control to control, not within a control. If you set the <a href="https://msdn.microsoft.com/e0a583da-c2bd-4757-868d-a63e697142e2">ACO_USETAB</a> flag in <i>dwFlag</i>, users can navigate to a string in the drop-down list by pressing the TAB key. If the drop-down list is closed, the TAB key allows the user to navigate from control to control, as usual. The user can close the drop-down list by pressing the ESC key.




## -see-also




<a href="https://msdn.microsoft.com/c093719f-7176-4ba4-ae75-399e8beeebf0">IAutoComplete2</a>



<a href="https://msdn.microsoft.com/00c2aa5f-eebc-479c-ac33-6efb3acb1051">IAutoComplete2::GetOptions</a>
 

 

