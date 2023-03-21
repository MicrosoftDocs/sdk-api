---
UID: NE:peninputpanel.__MIDL___MIDL_itf_peninputpanel_0000_0000_0006
title: InPlaceDirection (peninputpanel.h)
description: Specifies the preferred direction of the In-Place Input Panel relative to the text entry field.
helpviewer_keywords: ["798ad6d8-de1c-49dc-87a1-86bb4f73603a","InPlaceDirection","InPlaceDirection enumeration [Tablet PC]","InPlaceDirection_Auto","InPlaceDirection_Bottom","InPlaceDirection_Top","peninputpanel/InPlaceDirection","peninputpanel/InPlaceDirection_Auto","peninputpanel/InPlaceDirection_Bottom","peninputpanel/InPlaceDirection_Top","tablet.inplacedirection"]
old-location: tablet\inplacedirection.htm
tech.root: tablet
ms.assetid: 798ad6d8-de1c-49dc-87a1-86bb4f73603a
ms.date: 12/05/2018
ms.keywords: 798ad6d8-de1c-49dc-87a1-86bb4f73603a, InPlaceDirection, InPlaceDirection enumeration [Tablet PC], InPlaceDirection_Auto, InPlaceDirection_Bottom, InPlaceDirection_Top, peninputpanel/InPlaceDirection, peninputpanel/InPlaceDirection_Auto, peninputpanel/InPlaceDirection_Bottom, peninputpanel/InPlaceDirection_Top, tablet.inplacedirection
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
req.typenames: InPlaceDirection
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_peninputpanel_0000_0000_0006
 - peninputpanel/__MIDL___MIDL_itf_peninputpanel_0000_0000_0006
 - InPlaceDirection
 - peninputpanel/InPlaceDirection
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
 - InPlaceDirection
---

# InPlaceDirection enumeration


## -description

Specifies the preferred direction of the In-Place Input Panel relative to the text entry field.

## -enum-fields

### -field InPlaceDirection_Auto:0

Restores the system default.

### -field InPlaceDirection_Bottom:1

The preferred direction is above the text entry field.

### -field InPlaceDirection_Top:2

The preferred direction is below the text entry field.

## -remarks

An application can specify whether the In-Place Input Panel defaults appear above or below a text entry field by setting the <a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-get_preferredinplacedirection">ITextInputPanel::PreferredInPlaceDirection Property</a> to <b>InPlaceDirection_Bottom</b> or <b>InPlaceDirection_Top</b>. <b>ITextInputPanel::PreferredInPlaceDirection Property</b> is a preference because the In-Place Input Panel overrides the preference set by the application when necessary to keep Input Panel on the screen. The system default is to position the In-Place Input Panel below a text field when possible; otherwise it is positioned above. Setting the <b>ITextInputPanel::PreferredInPlaceDirection Property</b> to <b>InPlaceDirection_Auto</b> restores the system default.

## -see-also

<a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-get_preferredinplacedirection">ITextInputPanel::PreferredInPlaceDirection Property</a>
