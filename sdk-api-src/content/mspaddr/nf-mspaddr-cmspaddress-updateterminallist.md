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

# CMSPAddress::UpdateTerminalList


## -description


The 
<b>UpdateTerminalList</b> method populates the MSP's list of static terminals. It assumes that we have no static terminals available and it is always called in situations where this is true. This method uses DirectShow's "devenum" component and a static list of categories to discover monikers for static terminals. It uses the static 
<a href="https://msdn.microsoft.com/2a2a037a-753c-4dd4-b6ce-10b69f2e2421">CreateTerminal</a> methods on each type of terminal (see below) to actually create the terminals, possibly failing if the moniker in question is not acceptable (see below). For each successfully created terminal, it adds the terminal to the address' list. When this process is complete, devenum is released. An MSP that uses different static terminals than the ones created or that needs to use additional static terminals must override this method. The categories currently used here are CLSID_CWaveInClassManager, CLSID_CWaveOutClassManager, and CLSID_CVidCapClassManager. The method does not use categories that correspond to media types that the derived MSP does not support (this is checked automatically in the base class).


## -parameters






## -see-also




<a href="https://msdn.microsoft.com/864bf814-43dd-4d2b-a5a7-fff12520accb">CMSPAddress</a>
 

 

