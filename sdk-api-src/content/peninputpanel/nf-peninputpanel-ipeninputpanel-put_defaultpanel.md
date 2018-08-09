---
UID: NF:peninputpanel.IPenInputPanel.put_DefaultPanel
title: IPenInputPanel::put_DefaultPanel
author: windows-sdk-content
description: Deprecated. The PenInputPanel has been replaced by the Text Input Panel (TIP).Gets or sets the default panel type used for input within the PenInputPanel object.
old-location: tablet\peninputpanel_defaultpanel.htm
old-project: tablet
ms.assetid: 2b0ff320-02ce-4b23-ae47-91504c93ac24
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 2b0ff320-02ce-4b23-ae47-91504c93ac24, DefaultPanel property [Tablet PC], DefaultPanel property [Tablet PC],IPenInputPanel interface, IPenInputPanel interface [Tablet PC],DefaultPanel property, IPenInputPanel.DefaultPanel, IPenInputPanel.put_DefaultPanel, IPenInputPanel::DefaultPanel, IPenInputPanel::get_DefaultPanel, IPenInputPanel::put_DefaultPanel, PenInputPanel.get_DefaultPanel, PenInputPanel.put_DefaultPanel, get_DefaultPanel, peninputpanel/IPenInputPanel::DefaultPanel, peninputpanel/IPenInputPanel::get_DefaultPanel, peninputpanel/IPenInputPanel::put_DefaultPanel, put_DefaultPanel, tablet.peninputpanel_defaultpanel
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: EventMask
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IPenInputPanel.DefaultPanel
 - IPenInputPanel.get_DefaultPanel
 - IPenInputPanel.put_DefaultPanel
 - PenInputPanel.get_DefaultPanel
 - PenInputPanel.put_DefaultPanel
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: ADAM
---

# IPenInputPanel::put_DefaultPanel


## -description



Deprecated.  The <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a> has been replaced by the <a href="https://msdn.microsoft.com/867f2d6f-e63a-4c02-9370-3848a3b5c40a">Text Input Panel (TIP)</a>.

Gets or sets the default panel type used for input within the <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a> object.



This property is read/write.


## -parameters


## -remarks



<div class="alert"><b>Note</b>  The <b>DefaultPanel</b> property cannot be set to <a href="https://msdn.microsoft.com/fbf0ecce-0286-4d1b-99ba-9d28fc25da30">Inactive</a>.</div>
<div> </div>
The <a href="https://msdn.microsoft.com/fbf0ecce-0286-4d1b-99ba-9d28fc25da30">Handwriting</a> panel-also known as the writing pad-is the default input UI for a <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a>.

If the value of this property is <a href="https://msdn.microsoft.com/library/windows/hardware/mt637446">Default</a>, then the <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a> object uses the last panel type used for any pen input panel in any application. If all previous references to the pen input panel have been destroyed in all active applications, a new <b>PenInputPanel</b> object uses the <b>Handwriting</b> panel type.

If the panel is changed by setting the <a href="https://msdn.microsoft.com/536ba874-b9f9-45c9-bf9a-a64679afc861">CurrentPanel</a> property before the <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a> object becomes active for the first time, a <a href="https://msdn.microsoft.com/21d38406-7ed9-4741-a092-ed3a369dc0dc">PanelChanged</a> event occurs.

Setting the <b>DefaultPanel</b> property enables you to specify which type of panel shows by default in that instance of the <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a> object. If the value of this property is <a href="https://msdn.microsoft.com/fbf0ecce-0286-4d1b-99ba-9d28fc25da30">Handwriting</a> or <b>Keyboard</b>, then each time the panel is made visible, it uses the handwriting or keyboard panel type, respectively.

If you re-attach the <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a> to a different control and change the <b>DefaultPanel</b> property when the focus changes to the new control, be sure to set the <b>DefaultPanel</b> property before setting the <a href="https://msdn.microsoft.com/4ece9a88-dc5e-4c5c-bf75-ad22a3d3cfb5">AttachedEditWindow</a> property to ensure that the correct panel is displayed.




## -see-also




<a href="https://msdn.microsoft.com/536ba874-b9f9-45c9-bf9a-a64679afc861">CurrentPanel Property</a>



<a href="tablet.ipeninputpanel">IPenInputPanel</a>



<a href="https://msdn.microsoft.com/fbf0ecce-0286-4d1b-99ba-9d28fc25da30">PanelType Enumeration</a>



<a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a>
 

 

