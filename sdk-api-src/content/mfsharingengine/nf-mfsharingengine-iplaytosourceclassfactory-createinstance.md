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

# IPlayToSourceClassFactory::CreateInstance


## -description


Creates an instance of the <b>PlayToController</b> object.


## -parameters




### -param dwFlags [in]

A bitwise <b>OR</b> of flags from the <a href="https://msdn.microsoft.com/15B632DD-586B-40E4-9B63-05CCC6AFB93A">PLAYTO_SOURCE_CREATEFLAGS</a> enumeration.


### -param pControl [in]

A pointer to the <a href="https://msdn.microsoft.com/53355EEA-559B-4803-89F6-D454E15F9254">IPlayToControl</a> interface.


### -param ppSource






#### - ppController [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a> interface. The caller must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/F8F9FEC6-836C-429A-BADD-5CD1E550AED0">IPlayToSourceClassFactory</a>
 

 

