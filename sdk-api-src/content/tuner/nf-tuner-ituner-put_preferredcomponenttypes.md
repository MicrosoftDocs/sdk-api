---
UID: NF:tuner.ITuner.put_PreferredComponentTypes
title: ITuner::put_PreferredComponentTypes
author: windows-sdk-content
description: The put_PreferredComponentTypes method sets the collection of ComponentType objects used for default component selection.
old-location: mstv\ituner_put_preferredcomponenttypes.htm
old-project: mstv
ms.assetid: cca12a71-c842-4340-9233-f4143f6e0eea
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ITuner interface [Microsoft TV Technologies],put_PreferredComponentTypes method, ITuner.put_PreferredComponentTypes, ITuner::put_PreferredComponentTypes, ITunerput_PreferredComponentTypes, mstv.ituner_put_preferredcomponenttypes, put_PreferredComponentTypes, put_PreferredComponentTypes method [Microsoft TV Technologies], put_PreferredComponentTypes method [Microsoft TV Technologies],ITuner interface, tuner/ITuner::put_PreferredComponentTypes
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - ITuner.put_PreferredComponentTypes
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITuner::put_PreferredComponentTypes


## -description



The <b>put_PreferredComponentTypes</b> method sets the collection of <b>ComponentType</b> objects used for default component selection.




## -parameters




### -param ComponentTypes






#### - pComponentTypes [in]

Pointer to an <a href="https://msdn.microsoft.com/47c3837b-1348-4359-ad3d-3d82c5fe3781">IComponentTypes</a> interface that contains the collection of ComponentType objects.


## -returns



When the method is successful, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



Applications create a list of preferred component types by instantiating an empty <b>ComponentTypes</b> collection, filling it, then submitting it to the Tuner using <b>put_PreferredComponentTypes</b>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/1bc965a5-6bc9-488a-a2f9-f35d0cfbcccd">ITuner Interface</a>
 

 

