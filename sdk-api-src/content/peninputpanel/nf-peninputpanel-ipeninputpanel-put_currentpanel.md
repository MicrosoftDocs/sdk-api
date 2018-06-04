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

# IPenInputPanel::put_CurrentPanel


## -description



Deprecated.  The <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a> has been replaced by the <a href="https://msdn.microsoft.com/867f2d6f-e63a-4c02-9370-3848a3b5c40a">Text Input Panel (TIP)</a>.

Gets or sets which panel type is currently being used for input within the <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a> object.



This property is read/write.


## -parameters


## -remarks



<div class="alert"><b>Note</b>  The <b>CurrentPanel</b> property cannot be set to <a href="https://msdn.microsoft.com/library/windows/hardware/mt637446">Default</a> or <b>Inactive</b>, only <b>Handwriting</b> or <b>Keyboard</b>.</div>
<div> </div>
When you create a <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a> object, the <a href="https://msdn.microsoft.com/fbf0ecce-0286-4d1b-99ba-9d28fc25da30">Handwriting</a> panel - also known as the writing pad - is the default input UI.

If you change the panel by setting the <b>CurrentPanel</b> property before the <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a> object becomes active for the first time, a <a href="https://msdn.microsoft.com/21d38406-7ed9-4741-a092-ed3a369dc0dc">PanelChanged</a> event occurs.

<b>CurrentPanel</b> returns the <a href="https://msdn.microsoft.com/fbf0ecce-0286-4d1b-99ba-9d28fc25da30">Inactive</a> enumeration value if the panel window is associated with another instance of the <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a> object. Setting the <b>CurrentPanel</b> property raises an exception if the panel is inactive or if the panel type is invalid.




## -see-also




<a href="https://msdn.microsoft.com/2b0ff320-02ce-4b23-ae47-91504c93ac24">DefaultPanel Property</a>



<a href="tablet.ipeninputpanel">IPenInputPanel</a>



<a href="https://msdn.microsoft.com/fbf0ecce-0286-4d1b-99ba-9d28fc25da30">PanelType Enumeration</a>



<a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a>
 

 

