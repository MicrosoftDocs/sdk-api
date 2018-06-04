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

# InitMUILanguage function


## -description


Enables an application to specify a language to be used with the common controls that is different from the system language. 


## -parameters




### -param uiLang

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LANGID</a></b>

The  <a href="https://msdn.microsoft.com/076e2a43-256a-4646-a5c8-1d48ab08ce1a">language identifier</a> of the language to be used by the common controls. 


## -returns



None




## -remarks



This function enables an application to override the system language setting, and specify a different language for the common controls. The selected language only applies to the process that <b>InitMUILanguage</b> is called from. See <a href="https://msdn.microsoft.com/90dbbd70-3609-4c12-bdc1-7fa222c96f67">Internationalization for Windows Applications</a> for further discussion of localization.




## -see-also




<a href="https://msdn.microsoft.com/e034cd63-ffe5-4b48-8e23-248fe22b884a">GetMUILanguage</a>
 

 

