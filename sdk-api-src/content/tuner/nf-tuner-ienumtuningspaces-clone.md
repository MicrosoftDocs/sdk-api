---
UID: NF:tuner.IEnumTuningSpaces.Clone
title: IEnumTuningSpaces::Clone (tuner.h)
author: windows-sdk-content
description: The Clone method creates a new copy of the collection and all its sub-objects.
old-location: mstv\ienumtuningspaces_clone.htm
tech.root: mstv
ms.assetid: 3f9ad46e-38a7-4f07-b04b-999c912f9965
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Microsoft TV Technologies], Clone method [Microsoft TV Technologies],IEnumTuningSpaces interface, IEnumTuningSpaces interface [Microsoft TV Technologies],Clone method, IEnumTuningSpaces.Clone, IEnumTuningSpaces::Clone, IEnumTuningSpacesClone, mstv.ienumtuningspaces_clone, tuner/IEnumTuningSpaces::Clone
ms.topic: method
f1_keywords: 
 - "tuner/IEnumTuningSpaces.Clone"
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumTuningSpaces::Clone


## -description



The <b>Clone</b> method creates a new copy of the collection and all its sub-objects.




## -parameters




### -param ppEnum [out]

Address of an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ienumtuningspaces">IEnumTuningSpaces</a> interface pointer that will receive the returned interface.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ienumtuningspaces">IEnumTuningSpaces Interface</a>
 

 

