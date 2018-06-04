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

# ISpellChecker::add_SpellCheckerChanged


## -description


Adds an event handler (<a href="https://msdn.microsoft.com/9dd1f768-a901-4682-9530-019fe1dfbf0b">ISpellCheckerChangedEventHandler</a>) for the SpellCheckerChanged event.


## -parameters




### -param handler [in]

The handler to invoke when the spell checker changes.


### -param eventCookie [out, retval]

An event cookie that uniquely identifies the added handler. This cookie must be passed to <a href="https://msdn.microsoft.com/66f62590-2d86-4747-a9e8-ea02f26eeb4d">remove_SpellCheckerChanged</a> to stop this handler from being invoked by spell checker changes.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The SpellCheckerChanged event fires whenever the state of the spell checker changes in a way such that any text that has been checked should be rechecked. This should happen when the contents of a word list changes, when an option changes, or when the default spell checker changes.




## -see-also




<a href="https://msdn.microsoft.com/3cc5f675-048d-4ef3-9b66-5f081ee17a18">ISpellChecker</a>



<a href="https://msdn.microsoft.com/9dd1f768-a901-4682-9530-019fe1dfbf0b">ISpellCheckerChangedEventHandler</a>



<a href="https://msdn.microsoft.com/66f62590-2d86-4747-a9e8-ea02f26eeb4d">remove_SpellCheckerChanged</a>
 

 

