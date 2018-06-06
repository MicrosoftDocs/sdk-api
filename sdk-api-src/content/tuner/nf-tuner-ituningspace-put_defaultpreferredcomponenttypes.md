---
UID: NF:tuner.ITuningSpace.put_DefaultPreferredComponentTypes
title: ITuningSpace::put_DefaultPreferredComponentTypes
author: windows-sdk-content
description: The put_DefaultPreferredComponentTypes method specifies the default preferred component types for this tuning space.
old-location: mstv\ituningspace_put_defaultpreferredcomponenttypes.htm
old-project: mstv
ms.assetid: 11ab6f15-1f16-42f9-9d7f-f0e51c83cba3
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: ITuningSpace interface [Microsoft TV Technologies],put_DefaultPreferredComponentTypes method, ITuningSpace.put_DefaultPreferredComponentTypes, ITuningSpace::put_DefaultPreferredComponentTypes, ITuningSpaceput_DefaultPreferredComponentTypes, mstv.ituningspace_put_defaultpreferredcomponenttypes, put_DefaultPreferredComponentTypes, put_DefaultPreferredComponentTypes method [Microsoft TV Technologies], put_DefaultPreferredComponentTypes method [Microsoft TV Technologies],ITuningSpace interface, tuner/ITuningSpace::put_DefaultPreferredComponentTypes
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
 - ITuningSpace.put_DefaultPreferredComponentTypes
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITuningSpace::put_DefaultPreferredComponentTypes


## -description



The <b>put_DefaultPreferredComponentTypes</b> method specifies the default preferred component types for this tuning space.




## -parameters




### -param NewComponentTypes






#### - pNewComponentTypes [in]

Pointer to the <a href="https://msdn.microsoft.com/47c3837b-1348-4359-ad3d-3d82c5fe3781">IComponentTypes</a> interface of the component types collection.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/51850105-b3b1-4758-acde-05ca2f3439f2">ITuningSpace Interface</a>
 

 

