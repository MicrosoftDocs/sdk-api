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

# __MIDL___MIDL_itf_peninputpanel_0000_0000_0007 enumeration


## -description



The events on the <a href="https://msdn.microsoft.com/1e719900-db58-430d-9059-efb3f884f6f0">ITextInputPanel Interface</a> that you can set attention for.




## -enum-fields




### -field EventMask_InPlaceStateChanging


            Occurs when the correction mode is about to change.
          


### -field EventMask_InPlaceStateChanged


            Occurs when the correction mode has changed.
          


### -field EventMask_InPlaceSizeChanging


            Occurs when the in-place Input Panel size is about to change due to user resizing, auto growth or an input area change.
          


### -field EventMask_InPlaceSizeChanged


            Occurs when the in-place Input Panel size has changed due to a user resize, auto growth, or an input area change.
          


### -field EventMask_InputAreaChanging


            Occurs when the input area is about to change.
          


### -field EventMask_InputAreaChanged


            Occurs when the input area has changed.
          


### -field EventMask_CorrectionModeChanging


            Occurs when the correction mode is about to change.
          


### -field EventMask_CorrectionModeChanged


            Occurs when the correction mode has changed.
          


### -field EventMask_InPlaceVisibilityChanging


            Occurs when the in-place Input Panel visibility is about to change.
          


### -field EventMask_InPlaceVisibilityChanged


            Occurs when the input area has changed.
          


### -field EventMask_TextInserting


            Occurs when Tablet PC Input Panel is about to insert text into the control with input focus.
          


### -field EventMask_TextInserted


            Occurs when the Tablet PC Input Panel has inserted text into the control with input focus.
          


### -field EventMask_All


            Represents a bitwise combination of all member events.
          


## -see-also




<a href="https://msdn.microsoft.com/4ea32572-84e6-4230-a634-fc83cb86601f">ITextInputPanel::Advise Method</a>
 

 

