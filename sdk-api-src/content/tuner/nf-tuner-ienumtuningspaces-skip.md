---
UID: NF:tuner.IEnumTuningSpaces.Skip
title: IEnumTuningSpaces::Skip (tuner.h)
author: windows-sdk-content
description: The Skip method skips the specified element in the collection.
old-location: mstv\ienumtuningspaces_skip.htm
tech.root: mstv
ms.assetid: 5449fca0-4b8d-402e-b444-e7bc314e47b3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnumTuningSpaces interface [Microsoft TV Technologies],Skip method, IEnumTuningSpaces.Skip, IEnumTuningSpaces::Skip, IEnumTuningSpacesSkip, Skip, Skip method [Microsoft TV Technologies], Skip method [Microsoft TV Technologies],IEnumTuningSpaces interface, mstv.ienumtuningspaces_skip, tuner/IEnumTuningSpaces::Skip
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
 - IEnumTuningSpaces.Skip
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumTuningSpaces::Skip


## -description



The <b>Skip</b> method skips the specified element in the collection.




## -parameters




### -param celt [in]

The index of the element to skip.


## -returns



Returns S_OK if successful. This method will succeed even if <i>celt</i> is zero. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ienumtuningspaces">IEnumTuningSpaces Interface</a>
 

 

