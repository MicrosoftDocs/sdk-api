---
UID: NF:ocidl.IOleControlSite.OnControlInfoChanged
title: IOleControlSite::OnControlInfoChanged (ocidl.h)
description: Informs the container that the control's CONTROLINFO structure has changed and that the container should call the control's IOleControl::GetControlInfo for an update.
helpviewer_keywords: ["IOleControlSite interface [COM]","OnControlInfoChanged method","IOleControlSite.OnControlInfoChanged","IOleControlSite::OnControlInfoChanged","OnControlInfoChanged","OnControlInfoChanged method [COM]","OnControlInfoChanged method [COM]","IOleControlSite interface","_ctrl_iolecontrolsite_oncontrolinfochanged","com.iolecontrolsite_oncontrolinfochanged","ocidl/IOleControlSite::OnControlInfoChanged"]
old-location: com\iolecontrolsite_oncontrolinfochanged.htm
tech.root: com
ms.assetid: d9e915c0-3443-4464-9e3e-e1fbfe37e838
ms.date: 12/05/2018
ms.keywords: IOleControlSite interface [COM],OnControlInfoChanged method, IOleControlSite.OnControlInfoChanged, IOleControlSite::OnControlInfoChanged, OnControlInfoChanged, OnControlInfoChanged method [COM], OnControlInfoChanged method [COM],IOleControlSite interface, _ctrl_iolecontrolsite_oncontrolinfochanged, com.iolecontrolsite_oncontrolinfochanged, ocidl/IOleControlSite::OnControlInfoChanged
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
 - IOleControlSite::OnControlInfoChanged
 - ocidl/IOleControlSite::OnControlInfoChanged
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
 - IOleControlSite.OnControlInfoChanged
---

# IOleControlSite::OnControlInfoChanged


## -description

Informs the container that the control's <a href="/windows/desktop/api/ocidl/ns-ocidl-controlinfo">CONTROLINFO</a> structure has changed and that the container should call the control's <a href="/windows/desktop/api/ocidl/nf-ocidl-iolecontrol-getcontrolinfo">IOleControl::GetControlInfo</a> for an update.



## -returns

This method returns S_OK in all cases.

## -see-also

<a href="/windows/desktop/api/ocidl/nf-ocidl-iolecontrol-getcontrolinfo">IOleControl::GetControlInfo</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-iolecontrolsite">IOleControlSite</a>
