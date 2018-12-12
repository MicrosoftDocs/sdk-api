---
UID: NF:peninputpanel.IPenInputPanel.put_CurrentPanel
title: IPenInputPanel::put_CurrentPanel
author: windows-sdk-content
description: Deprecated. The PenInputPanel has been replaced by the Text Input Panel (TIP).Gets or sets which panel type is currently being used for input within the PenInputPanel object.
old-location: tablet\peninputpanel_currentpanel.htm
tech.root: tablet
ms.assetid: 536ba874-b9f9-45c9-bf9a-a64679afc861
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 536ba874-b9f9-45c9-bf9a-a64679afc861, CurrentPanel property [Tablet PC], CurrentPanel property [Tablet PC],IPenInputPanel interface, IPenInputPanel interface [Tablet PC],CurrentPanel property, IPenInputPanel.CurrentPanel, IPenInputPanel.put_CurrentPanel, IPenInputPanel::CurrentPanel, IPenInputPanel::get_CurrentPanel, IPenInputPanel::put_CurrentPanel, PenInputPanel.get_CurrentPanel, PenInputPanel.put_CurrentPanel, get_CurrentPanel, peninputpanel/IPenInputPanel::CurrentPanel, peninputpanel/IPenInputPanel::get_CurrentPanel, peninputpanel/IPenInputPanel::put_CurrentPanel, put_CurrentPanel, tablet.peninputpanel_currentpanel
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: peninputpanel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: InkObj.dll
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IPenInputPanel.CurrentPanel
 - IPenInputPanel.get_CurrentPanel
 - IPenInputPanel.put_CurrentPanel
 - PenInputPanel.get_CurrentPanel
 - PenInputPanel.put_CurrentPanel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPenInputPanel::put_CurrentPanel


## -description



Deprecated.  The <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a> has been replaced by the <a href="https://msdn.microsoft.com/867f2d6f-e63a-4c02-9370-3848a3b5c40a">Text Input Panel (TIP)</a>.

Gets or sets which panel type is currently being used for input within the <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a> object.



This property is read/write.


## -parameters


## -remarks



<div class="alert"><b>Note</b>  The <b>CurrentPanel</b> property cannot be set to <a href="https://msdn.microsoft.com/fbf0ecce-0286-4d1b-99ba-9d28fc25da30">Default</a> or <b>Inactive</b>, only <b>Handwriting</b> or <b>Keyboard</b>.</div>
<div> </div>
When you create a <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a> object, the <a href="https://msdn.microsoft.com/fbf0ecce-0286-4d1b-99ba-9d28fc25da30">Handwriting</a> panel - also known as the writing pad - is the default input UI.

If you change the panel by setting the <b>CurrentPanel</b> property before the <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a> object becomes active for the first time, a <a href="https://msdn.microsoft.com/21d38406-7ed9-4741-a092-ed3a369dc0dc">PanelChanged</a> event occurs.

<b>CurrentPanel</b> returns the <a href="https://msdn.microsoft.com/fbf0ecce-0286-4d1b-99ba-9d28fc25da30">Inactive</a> enumeration value if the panel window is associated with another instance of the <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a> object. Setting the <b>CurrentPanel</b> property raises an exception if the panel is inactive or if the panel type is invalid.




## -see-also




<a href="https://msdn.microsoft.com/2b0ff320-02ce-4b23-ae47-91504c93ac24">DefaultPanel Property</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt846809(v=VS.85).aspx">IPenInputPanel</a>



<a href="https://msdn.microsoft.com/fbf0ecce-0286-4d1b-99ba-9d28fc25da30">PanelType Enumeration</a>



<a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a>
 

 

