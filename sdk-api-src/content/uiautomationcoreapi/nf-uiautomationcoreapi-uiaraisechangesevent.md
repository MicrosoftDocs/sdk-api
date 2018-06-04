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

# UiaRaiseChangesEvent function


## -description


Called by providers to notify the Microsoft UI Automation core that a change has occurred.


## -parameters




### -param pProvider [in]

Type: <b><a href="https://msdn.microsoft.com/f0ec6185-acd0-4df7-88f4-fd00747f98bf">IRawElementProviderSimple</a>*</b>

The provider node where the change event occurred.


### -param eventIdCount [in]

The number of changes that occurred. This is the number of <a href="https://msdn.microsoft.com/28C0C0DE-7ED2-4D01-B532-E56AD81AE8D0">UiaChangeInfo</a> structures pointed to by the <i>pUiaChanges</i> parameter.


### -param pUiaChanges [in]

A collection of pointers to <a href="https://msdn.microsoft.com/28C0C0DE-7ED2-4D01-B532-E56AD81AE8D0">UiaChangeInfo</a> structures.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

<a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a> value indicating success or failure.



