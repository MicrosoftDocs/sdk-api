---
UID: NF:tuner.ITuningSpaceContainer.Remove
title: ITuningSpaceContainer::Remove
author: windows-driver-content
description: The Remove method permanently removes a tuning space from the system.
old-location: mstv\ituningspacecontainer_remove.htm
old-project: mstv
ms.assetid: 72ead181-6c5a-49d1-a789-3ae4128417c6
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: ITuningSpaceContainer interface [Microsoft TV Technologies],Remove method, ITuningSpaceContainer.Remove, ITuningSpaceContainer::Remove, ITuningSpaceContainerRemove, Remove, Remove method [Microsoft TV Technologies], Remove method [Microsoft TV Technologies],ITuningSpaceContainer interface, mstv.ituningspacecontainer_remove, tuner/ITuningSpaceContainer::Remove
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	ITuningSpaceContainer.Remove
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITuningSpaceContainer::Remove


## -description



The <b>Remove</b> method permanently removes a tuning space from the system.




## -parameters




### -param Index [in]

Variable of type <b>VARIANT</b> that specifies the ID of the tuning space to remove.


## -returns



Returns S_OK if successful. If the specified tuning space was invalid or corrupted in the Registry, this method will delete whatever information is there and return S_FALSE.




## -see-also




<a href="https://msdn.microsoft.com/8f053c53-2a2b-4d98-a510-c516faa21611">ITuningSpaceContainer Interface</a>
 

 

