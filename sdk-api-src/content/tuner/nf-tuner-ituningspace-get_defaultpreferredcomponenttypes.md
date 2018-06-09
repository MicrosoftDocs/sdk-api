---
UID: NF:tuner.ITuningSpace.get_DefaultPreferredComponentTypes
title: ITuningSpace::get_DefaultPreferredComponentTypes
author: windows-sdk-content
description: The get_DefaultPreferredComponentTypes method returns an list of the default preferred component types for this tuning space.
old-location: mstv\ituningspace_get_defaultpreferredcomponenttypes.htm
old-project: mstv
ms.assetid: a633a94c-e514-46b1-9982-7526ffa89b74
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: ITuningSpace interface [Microsoft TV Technologies],get_DefaultPreferredComponentTypes method, ITuningSpace.get_DefaultPreferredComponentTypes, ITuningSpace::get_DefaultPreferredComponentTypes, ITuningSpaceget_DefaultPreferredComponentTypes, get_DefaultPreferredComponentTypes, get_DefaultPreferredComponentTypes method [Microsoft TV Technologies], get_DefaultPreferredComponentTypes method [Microsoft TV Technologies],ITuningSpace interface, mstv.ituningspace_get_defaultpreferredcomponenttypes, tuner/ITuningSpace::get_DefaultPreferredComponentTypes
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
 - ITuningSpace.get_DefaultPreferredComponentTypes
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITuningSpace::get_DefaultPreferredComponentTypes


## -description



The <b>get_DefaultPreferredComponentTypes</b> method returns an list of the default preferred component types for this tuning space.




## -parameters




### -param ComponentTypes






#### - ppComponentTypes [out]

Address of a variable that receives an <a href="https://msdn.microsoft.com/47c3837b-1348-4359-ad3d-3d82c5fe3781">IComponentTypes</a> interface pointer. Use this interface to enumerate the component types. The caller must release the interface.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



A component is a stream within the program. An example of a preferred component type would be an audio stream in English. When multiple components are available, the Tuner attempts to play the preferred ones first.

If the tuning space does not have any default preferred types, this method succeeds but returns the value <b>NULL</b> in the <i>ppComponentTypes</i> parameter. Check for a <b>NULL</b> value before attempting to dereference the pointer.




## -see-also




<a href="https://msdn.microsoft.com/51850105-b3b1-4758-acde-05ca2f3439f2">ITuningSpace Interface</a>
 

 

