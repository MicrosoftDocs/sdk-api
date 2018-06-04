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

# __MIDL_ITfCandidateList_0001 enumeration


## -description


Elements of the <b>TfCandidateResult</b> enumeration are used with the <a href="https://msdn.microsoft.com/dcc172f9-4fc3-46f4-a1db-0e75fceafb28">ITfCandidateList::SetResult</a> method to specify the result of a reconversion operation performed on a given candidate string.


## -enum-fields




### -field CAND_FINALIZED

The candidate string has been selected and accepted. The previous text should be replaced with the specified candidate.


### -field CAND_SELECTED

The candidate string has been selected, but the selection is not yet final.


### -field CAND_CANCELED

The reconversion operation has been canceled.


## -see-also




<a href="https://msdn.microsoft.com/dcc172f9-4fc3-46f4-a1db-0e75fceafb28">ITfCandidateList::SetResult
      </a>
 

 

