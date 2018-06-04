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

# GetMUILanguage function


## -description


Gets the language currently in use by the common controls for a particular process. 


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LANGID</a></b>

Returns the <a href="https://msdn.microsoft.com/076e2a43-256a-4646-a5c8-1d48ab08ce1a">language identifier</a> of the language an application has specified for the common controls by calling <a href="https://msdn.microsoft.com/67ad64fa-bb05-4c04-8b57-0dc4a0f87cdb">InitMUILanguage</a>. <b>GetMUILanguage</b> returns the value for the process from which it is called. If 
						<b>InitMUILanguage</b> has not been called or was not called from the same process, <b>GetMUILanguage</b> returns the language-neutral LANGID, <a href="https://msdn.microsoft.com/cdf6424a-bf2b-4c14-8bc7-8b5f04c29ed3">MAKELANGID</a>(LANG_NEUTRAL, SUBLANG_NEUTRAL).




## -remarks



See <a href="https://msdn.microsoft.com/90dbbd70-3609-4c12-bdc1-7fa222c96f67">Internationalization for Windows Applications</a> for further discussion of localization.



