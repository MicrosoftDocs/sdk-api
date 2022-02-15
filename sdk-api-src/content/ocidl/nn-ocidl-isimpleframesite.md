---
UID: NN:ocidl.ISimpleFrameSite
title: ISimpleFrameSite (ocidl.h)
description: Provides simple frame controls that act as simple containers for other nested controls.
helpviewer_keywords: ["ISimpleFrameSite","ISimpleFrameSite interface [COM]","ISimpleFrameSite interface [COM]","described","_ctrl_isimpleframesite","com.isimpleframesite","ocidl/ISimpleFrameSite"]
old-location: com\isimpleframesite.htm
tech.root: com
ms.assetid: ccddeae4-14fc-47df-a612-83d48a479b48
ms.date: 12/05/2018
ms.keywords: ISimpleFrameSite, ISimpleFrameSite interface [COM], ISimpleFrameSite interface [COM],described, _ctrl_isimpleframesite, com.isimpleframesite, ocidl/ISimpleFrameSite
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISimpleFrameSite
 - ocidl/ISimpleFrameSite
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - ISimpleFrameSite
---

# ISimpleFrameSite interface


## -description

Provides simple frame controls that act as simple containers for other nested controls. Some controls merely contain other controls. In such cases, the simple control container, called a simple frame, need not implement all container requirements. It can delegate most of the interface calls from its contained controls to the outer container that manages the simple frame. To support what are called simple frame controls, a container implements this interface as well as other site interfaces such as <a href="/windows/desktop/api/ocidl/nn-ocidl-iolecontrolsite">IOleControlSite</a>.

An example of a simple frame control is a group box that only needs to capture a few keystrokes for its contained controls to implement the correct tab or arrow key behavior, but does not want to handle every other message. Through the two methods of this interface, the simple frame control passes messages to its control site both before and after its own processing. If that site is itself a simple frame, it can continue to pass messages up the chain.

## -inheritance

The <b>ISimpleFrameSite</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISimpleFrameSite</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-iolecontrol">IOleControl</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-iolecontrolsite">IOleControlSite</a>
