---
UID: NE:termmgr.__MIDL___MIDL_itf_termmgr_0000_0000_0001
title: "__MIDL___MIDL_itf_termmgr_0000_0000_0001"
author: windows-sdk-content
description: The TMGR_DIRECTION enum is used by the pluggable terminal methods to indicate terminal direction.
old-location: tapi3\tmgr_direction.htm
old-project: Tapi
ms.assetid: 1758efb7-55fc-4925-be56-7f43177db64f
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: TMGR_DIRECTION, TMGR_DIRECTION enumeration [TAPI 2.2], TMGR_TD_BOTH, TMGR_TD_CAPTURE, TMGR_TD_RENDER, __MIDL___MIDL_itf_termmgr_0000_0000_0001, _tapi3_tmgr_direction, tapi3.tmgr_direction, termmgr/TMGR_DIRECTION, termmgr/TMGR_TD_BOTH, termmgr/TMGR_TD_CAPTURE, termmgr/TMGR_TD_RENDER
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: TMGR_DIRECTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Termmgr.h
api_name:
 - TMGR_DIRECTION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# __MIDL___MIDL_itf_termmgr_0000_0000_0001 enumeration


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




<a href="https://msdn.microsoft.com/67f2f241-2389-476f-a412-af456c1c3376">ITPluggableTerminalClassRegistration::get_Direction</a>



<a href="https://msdn.microsoft.com/b68c0697-e889-471d-857a-d11e974c6552">ITPluggableTerminalClassRegistration::put_Direction</a>
 

 

