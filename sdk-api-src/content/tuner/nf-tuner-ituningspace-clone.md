---
UID: NF:tuner.ITuningSpace.Clone
title: ITuningSpace::Clone
author: windows-sdk-content
description: The Clone method creates a new copy of the tuning space.
old-location: mstv\ituningspace_clone.htm
old-project: mstv
ms.assetid: 01dcde87-b043-491e-b5cf-9800c12b5335
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: Clone, Clone method [Microsoft TV Technologies], Clone method [Microsoft TV Technologies],ITuningSpace interface, ITuningSpace interface [Microsoft TV Technologies],Clone method, ITuningSpace.Clone, ITuningSpace::Clone, ITuningSpaceClone, mstv.ituningspace_clone, tuner/ITuningSpace::Clone
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
 - ITuningSpace.Clone
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITuningSpace::Clone


## -description



The <b>Clone</b> method creates a new copy of the tuning space.




## -parameters




### -param NewTS






#### - ppNewTS [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/51850105-b3b1-4758-acde-05ca2f3439f2">ITuningSpace</a> interface of the new tuning space object. The caller must release the interface.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/51850105-b3b1-4758-acde-05ca2f3439f2">ITuningSpace Interface</a>
 

 

