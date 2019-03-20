---
UID: NF:tuner.ITuner.get_PreferredComponentTypes
title: ITuner::get_PreferredComponentTypes (tuner.h)
author: windows-sdk-content
description: The get_PreferredComponentTypes method gets the collection of ComponentType objects used for default component selection.
old-location: mstv\ituner_get_preferredcomponenttypes.htm
tech.root: mstv
ms.assetid: 1ed2d1b5-8ba3-4230-8cc3-f8207635a78a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITuner interface [Microsoft TV Technologies],get_PreferredComponentTypes method, ITuner.get_PreferredComponentTypes, ITuner::get_PreferredComponentTypes, ITunerget_PreferredComponentTypes, get_PreferredComponentTypes, get_PreferredComponentTypes method [Microsoft TV Technologies], get_PreferredComponentTypes method [Microsoft TV Technologies],ITuner interface, mstv.ituner_get_preferredcomponenttypes, tuner/ITuner::get_PreferredComponentTypes
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
 - ITuner.get_PreferredComponentTypes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITuner::get_PreferredComponentTypes


## -description



The <b>get_PreferredComponentTypes</b> method gets the collection of ComponentType objects used for default component selection.




## -parameters




### -param ComponentTypes [out]

Address of an <a href="https://msdn.microsoft.com/47c3837b-1348-4359-ad3d-3d82c5fe3781">IComponentTypes</a> interface pointer that receives the collection of ComponentType objects.


## -returns



When the method is successful, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



When a program ends, there may be a new set of stream components available, so at that time the tuner will automatically examine the list of preferred component types and select a component based on that list. If no list is available, the tuner will make a selection based on other factors. Applications call this method simply to examine the current list.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/1bc965a5-6bc9-488a-a2f9-f35d0cfbcccd">ITuner Interface</a>
 

 

