---
UID: NE:peninputpanel.PanelType
title: PanelType (peninputpanel.h)
description: Defines the type of input currently available in the PenInputPanel object.
helpviewer_keywords: ["PT_Default","PT_Handwriting","PT_Inactive","PT_Keyboard","PanelType","PanelType enumeration [Tablet PC]","fbf0ecce-0286-4d1b-99ba-9d28fc25da30","peninputpanel/PT_Default","peninputpanel/PT_Handwriting","peninputpanel/PT_Inactive","peninputpanel/PT_Keyboard","peninputpanel/PanelType","tablet.paneltype"]
old-location: tablet\paneltype.htm
tech.root: tablet
ms.assetid: fbf0ecce-0286-4d1b-99ba-9d28fc25da30
ms.date: 12/05/2018
ms.keywords: PT_Default, PT_Handwriting, PT_Inactive, PT_Keyboard, PanelType, PanelType enumeration [Tablet PC], fbf0ecce-0286-4d1b-99ba-9d28fc25da30, peninputpanel/PT_Default, peninputpanel/PT_Handwriting, peninputpanel/PT_Inactive, peninputpanel/PT_Keyboard, peninputpanel/PanelType, tablet.paneltype
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: PanelType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PanelType
 - peninputpanel/PanelType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - peninputpanel.h
api_name:
 - PanelType
---

# PanelType enumeration


## -description

Defines the type of input currently available in the <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> object.

## -enum-fields

### -field PT_Default:0

The <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> object displays the last panel type used for any pen input panel in any application. If all previous references to the pen input panel have been destroyed in all active applications, a new pen input panel will use the handwriting panel type.

### -field PT_Inactive

The <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> object does not accept input. This value is returned by the <a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_currentpanel">CurrentPanel</a> property when the panel window is owned by another instance of the <b>PenInputPanel</b> object. This value is also returned if the panel window has not yet been activated.

### -field PT_Handwriting

The <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> object displays the default handwriting panel for the current input language.

### -field PT_Keyboard

The <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> object displays the default keyboard panel for the current input language.

## -remarks

The end user can change the handwriting panel between lined and boxed input modes using buttons on the Tablet PC Input Panel user interface (UI). There is no programmatic way to get or set lined or boxed mode. By default, western languages use lined input and East Asian languages use boxed input, but the user is free to change between these modes.

## -see-also

<a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_currentpanel">CurrentPanel Property</a>



<a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_defaultpanel">DefaultPanel Property</a>



<a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel Class</a>
