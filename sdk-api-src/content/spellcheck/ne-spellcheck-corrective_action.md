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

# CORRECTIVE_ACTION enumeration


## -description


Identifies the type of corrective action to be taken for a spelling error.


## -enum-fields




### -field CORRECTIVE_ACTION_NONE

There are no errors.


### -field CORRECTIVE_ACTION_GET_SUGGESTIONS

The user should be prompted with a list of suggestions as returned by <a href="https://msdn.microsoft.com/bd6b1d90-8dc0-4640-a43a-678b43e55cb5">ISpellChecker::Suggest</a>.


### -field CORRECTIVE_ACTION_REPLACE

Replace the indicated erroneous text with the text provided in the suggestion. The user does not need to be prompted.


### -field CORRECTIVE_ACTION_DELETE

The user should be prompted to delete the indicated erroneous text.


## -see-also




<a href="https://msdn.microsoft.com/bd6b1d90-8dc0-4640-a43a-678b43e55cb5">ISpellChecker::Suggest</a>



<a href="https://msdn.microsoft.com/9b28d194-01a3-4ea2-8428-d2e91e6abad8">ISpellingError::CorrectiveAction</a>
 

 

