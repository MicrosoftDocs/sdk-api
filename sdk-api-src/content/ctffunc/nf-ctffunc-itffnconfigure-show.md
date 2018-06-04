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

# ITfFnConfigure::Show


## -description




## -parameters




### -param hwndParent [in]

Handle of the parent window. The text service typically uses this as the parent or owner window when creating a dialog box.


### -param langid [in]

Contains a <b>LANGID</b> value that specifies the identifier of the language selected in the Text Services control panel application.


### -param rguidProfile [in]

Contains a GUID value that specifies the language profile identifier that the text service is under. This is the value specified in <a href="https://msdn.microsoft.com/d132bff1-24de-4e43-859b-2425ba7de8f0">ITfInputProcessorProfiles::AddLanguageProfile</a> when the profile was added.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method should not return until the user closes the dialog box or property sheet.




## -see-also




<a href="https://msdn.microsoft.com/af23e668-9c00-4e53-89b6-c8be85ae961b">ITfFnConfigure</a>



<a href="https://msdn.microsoft.com/d132bff1-24de-4e43-859b-2425ba7de8f0">ITfInputProcessorProfiles::AddLanguageProfile
      </a>
 

 

