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

# __MIDL___MIDL_itf_peninputpanel_0000_0000_0006 enumeration


## -description



Specifies the preferred direction of the In-Place Input Panel relative to the text entry field.




## -enum-fields




### -field InPlaceDirection_Auto

Restores the system default.


### -field InPlaceDirection_Bottom

The preferred direction is above the text entry field.


### -field InPlaceDirection_Top

The preferred direction is below the text entry field.


## -remarks



An application can specify whether the In-Place Input Panel defaults appear above or below a text entry field by setting the <a href="https://msdn.microsoft.com/5d05e315-4e6d-4591-83d8-9cc98f2c2e2b">ITextInputPanel::PreferredInPlaceDirection Property</a> to <b>InPlaceDirection_Bottom</b> or <b>InPlaceDirection_Top</b>. <b>ITextInputPanel::PreferredInPlaceDirection Property</b> is a preference because the In-Place Input Panel overrides the preference set by the application when necessary to keep Input Panel on the screen. The system default is to position the In-Place Input Panel below a text field when possible; otherwise it is positioned above. Setting the <b>ITextInputPanel::PreferredInPlaceDirection Property</b> to <b>InPlaceDirection_Auto</b> restores the system default.




## -see-also




<a href="https://msdn.microsoft.com/5d05e315-4e6d-4591-83d8-9cc98f2c2e2b">ITextInputPanel::PreferredInPlaceDirection Property</a>
 

 

