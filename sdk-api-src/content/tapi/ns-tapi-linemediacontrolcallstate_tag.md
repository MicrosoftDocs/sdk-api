---
UID: NS:tapi.linemediacontrolcallstate_tag
title: linemediacontrolcallstate_tag
author: windows-sdk-content
description: The LINEMEDIACONTROLCALLSTATE structure describes a media action to be executed when detecting transitions into one or more call states. The lineSetMediaControl and TSPI_lineSetMediaControl functions use this structure.
old-location: tapi2\linemediacontrolcallstate_str.htm
tech.root: tapi
ms.assetid: c0768c2a-3015-41af-b32f-0b228a0f2ee6
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: "*LPLINEMEDIACONTROLCALLSTATE, LINEMEDIACONTROLCALLSTATE, LINEMEDIACONTROLCALLSTATE structure [TAPI 2.2], LPLINEMEDIACONTROLCALLSTATE, LPLINEMEDIACONTROLCALLSTATE structure pointer [TAPI 2.2], _tapi2_linemediacontrolcallstate_str, linemediacontrolcallstate_tag, tapi/LINEMEDIACONTROLCALLSTATE, tapi/LPLINEMEDIACONTROLCALLSTATE, tapi2.linemediacontrolcallstate_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: tapi.h
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
 - Tapi.h
api_name:
 - LINEMEDIACONTROLCALLSTATE
product: Windows
targetos: Windows
req.typenames: LINEMEDIACONTROLCALLSTATE, *LPLINEMEDIACONTROLCALLSTATE
req.redist: 
---

# linemediacontrolcallstate_tag structure


## -description


The 
<b>LINEMEDIACONTROLCALLSTATE</b> structure describes a media action to be executed when detecting transitions into one or more call states. The 
<a href="https://msdn.microsoft.com/5a4fc83a-6bc9-4081-b374-ddb912fb2242">lineSetMediaControl</a> and 
<a href="https://msdn.microsoft.com/e9273bd6-8dc3-4b45-bf0e-a1a10d78a604">TSPI_lineSetMediaControl</a> functions use this structure.


## -struct-fields




### -field dwCallStates

One or more call states. This member uses one of the 
<a href="https://msdn.microsoft.com/18d881ee-cf98-4dec-a561-333c2518935d">LINECALLSTATE_ Constants</a>.


### -field dwMediaControl

Media control action. This member uses one of the 
<a href="https://msdn.microsoft.com/1e8aeda8-2810-462a-bfba-0296d854d9aa">LINEMEDIACONTROL_ Constants</a>.


## -remarks



This structure may not be extended.

The 
<b>LINEMEDIACONTROLCALLSTATE</b> structure defines a triple &lt;call state(s), media-control action&gt;. An array of these triples is passed to the 
<a href="https://msdn.microsoft.com/5a4fc83a-6bc9-4081-b374-ddb912fb2242">lineSetMediaControl</a> function to set the media control actions triggered by the transition to the call state of the given call. When a transition to a listed call state is detected, the corresponding action on the media stream is invoked.




## -see-also




<a href="https://msdn.microsoft.com/e9273bd6-8dc3-4b45-bf0e-a1a10d78a604">TSPI_lineSetMediaControl</a>



<a href="https://msdn.microsoft.com/aa407269-06be-43e2-906e-20137e4bdb89">lineGenerateDigits</a>



<a href="https://msdn.microsoft.com/5a4fc83a-6bc9-4081-b374-ddb912fb2242">lineSetMediaControl</a>
 

 

