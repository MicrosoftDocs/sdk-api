---
UID: NF:tuner.IEnumTuningSpaces.Clone
title: IEnumTuningSpaces::Clone
author: windows-sdk-content
description: The Clone method creates a new copy of the collection and all its sub-objects.
old-location: mstv\ienumtuningspaces_clone.htm
old-project: mstv
ms.assetid: 3f9ad46e-38a7-4f07-b04b-999c912f9965
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: Clone, Clone method [Microsoft TV Technologies], Clone method [Microsoft TV Technologies],IEnumTuningSpaces interface, IEnumTuningSpaces interface [Microsoft TV Technologies],Clone method, IEnumTuningSpaces.Clone, IEnumTuningSpaces::Clone, IEnumTuningSpacesClone, mstv.ienumtuningspaces_clone, tuner/IEnumTuningSpaces::Clone
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IEnumTuningSpaces.Clone
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IEnumTuningSpaces::Clone


## -description



The <b>Clone</b> method creates a new copy of the collection and all its sub-objects.




## -parameters




### -param ppEnum [out]

Address of an <a href="https://msdn.microsoft.com/9b64a48f-ebab-46af-a89d-b8bc488d85da">IEnumTuningSpaces</a> interface pointer that will receive the returned interface.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/9b64a48f-ebab-46af-a89d-b8bc488d85da">IEnumTuningSpaces Interface</a>
 

 

