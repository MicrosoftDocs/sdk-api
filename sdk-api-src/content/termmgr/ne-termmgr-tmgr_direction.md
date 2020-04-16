---
UID: NE:termmgr.__MIDL___MIDL_itf_termmgr_0000_0000_0001
title: TMGR_DIRECTION (termmgr.h)
description: The TMGR_DIRECTION enum is used by the pluggable terminal methods to indicate terminal direction.helpviewer_keywords: ["TMGR_DIRECTION","TMGR_DIRECTION enumeration [TAPI 2.2]","TMGR_TD_BOTH","TMGR_TD_CAPTURE","TMGR_TD_RENDER","_tapi3_tmgr_direction","tapi3.tmgr_direction","termmgr/TMGR_DIRECTION","termmgr/TMGR_TD_BOTH","termmgr/TMGR_TD_CAPTURE","termmgr/TMGR_TD_RENDER"]
old-location: tapi3\tmgr_direction.htm
tech.root: Tapi
ms.assetid: 1758efb7-55fc-4925-be56-7f43177db64f
ms.date: 12/05/2018
ms.keywords: TMGR_DIRECTION, TMGR_DIRECTION enumeration [TAPI 2.2], TMGR_TD_BOTH, TMGR_TD_CAPTURE, TMGR_TD_RENDER, _tapi3_tmgr_direction, tapi3.tmgr_direction, termmgr/TMGR_DIRECTION, termmgr/TMGR_TD_BOTH, termmgr/TMGR_TD_CAPTURE, termmgr/TMGR_TD_RENDER
f1_keywords:
- termmgr/TMGR_DIRECTION
dev_langs:
- c++
req.header: termmgr.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Termmgr.h
api_name:
- TMGR_DIRECTION
targetos: Windows
req.typenames: TMGR_DIRECTION
req.redist: 
ms.custom: 19H1
---

# TMGR_DIRECTION enumeration


## -description


The 
<b>TMGR_DIRECTION</b> enum is used by the pluggable terminal methods to indicate terminal direction.


## -enum-fields




### -field TMGR_TD_CAPTURE

The terminal can originate a media stream.


### -field TMGR_TD_RENDER

The terminal can render a media stream.


### -field TMGR_TD_BOTH

The terminal can handle both directions of a media stream.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nf-termmgr-itpluggableterminalclassregistration-get_direction">ITPluggableTerminalClassRegistration::get_Direction</a>



<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nf-termmgr-itpluggableterminalclassregistration-put_direction">ITPluggableTerminalClassRegistration::put_Direction</a>
 

 

