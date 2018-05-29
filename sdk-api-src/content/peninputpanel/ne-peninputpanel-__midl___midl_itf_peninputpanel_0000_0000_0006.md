---
UID: NE:peninputpanel.__MIDL___MIDL_itf_peninputpanel_0000_0000_0006
title: "__MIDL___MIDL_itf_peninputpanel_0000_0000_0006"
author: windows-sdk-content
description: Specifies the preferred direction of the In-Place Input Panel relative to the text entry field.
old-location: tablet\inplacedirection.htm
old-project: tablet
ms.assetid: 798ad6d8-de1c-49dc-87a1-86bb4f73603a
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: 798ad6d8-de1c-49dc-87a1-86bb4f73603a, InPlaceDirection, InPlaceDirection enumeration [Tablet PC], InPlaceDirection_Auto, InPlaceDirection_Bottom, InPlaceDirection_Top, __MIDL___MIDL_itf_peninputpanel_0000_0000_0006, peninputpanel/InPlaceDirection, peninputpanel/InPlaceDirection_Auto, peninputpanel/InPlaceDirection_Bottom, peninputpanel/InPlaceDirection_Top, tablet.inplacedirection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
req.typenames: InPlaceDirection
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	peninputpanel.h
api_name:
-	InPlaceDirection
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
 

 

