---
UID: NF:oleidl.IOleInPlaceFrame.EnableModeless
title: IOleInPlaceFrame::EnableModeless
author: windows-sdk-content
description: Enables or disables a frame's modeless dialog boxes.
old-location: com\ioleinplaceframe_enablemodeless.htm
tech.root: com
ms.assetid: 4c6ea1ee-861d-45ff-a9d2-d3b241f00c9f
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: EnableModeless, EnableModeless method [COM], EnableModeless method [COM],IOleInPlaceFrame interface, IOleInPlaceFrame interface [COM],EnableModeless method, IOleInPlaceFrame.EnableModeless, IOleInPlaceFrame::EnableModeless, _ole_ioleinplaceframe_enablemodeless, com.ioleinplaceframe_enablemodeless, oleidl/IOleInPlaceFrame::EnableModeless
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
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
 - COM
api_location:
 - OleIdl.h
api_name:
 - IOleInPlaceFrame.EnableModeless
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOleInPlaceFrame::EnableModeless


## -description


Enables or disables a frame's modeless dialog boxes.


## -parameters




### -param fEnable [in]

Specifies whether the modeless dialog box windows are to be enabled (<b>TRUE</b>) or disabled (<b>FALSE</b>).


## -returns



This method returns S_OK if the dialog box was either enabled or disabled successfully, depending on the value for <i>fEnable</i>.




## -see-also




<a href="https://msdn.microsoft.com/2fc45490-b3fe-48fd-a41c-2b7f35b09edc">IOleInPlaceActiveObject::EnableModeless</a>



<a href="https://msdn.microsoft.com/c530aff7-fd83-413d-8945-0c9d1bfb51ba">IOleInPlaceFrame</a>
 

 

