---
UID: NF:ocidl.IOleControlSite.OnFocus
title: IOleControlSite::OnFocus (ocidl.h)
description: Indicates whether the control managed by this control site has gained or lost the focus.
helpviewer_keywords: ["IOleControlSite interface [COM]","OnFocus method","IOleControlSite.OnFocus","IOleControlSite::OnFocus","OnFocus","OnFocus method [COM]","OnFocus method [COM]","IOleControlSite interface","_ctrl_iolecontrolsite_onfocus","com.iolecontrolsite_onfocus","ocidl/IOleControlSite::OnFocus"]
old-location: com\iolecontrolsite_onfocus.htm
tech.root: com
ms.assetid: 22869326-2815-49cb-8d03-14dca5d45689
ms.date: 12/05/2018
ms.keywords: IOleControlSite interface [COM],OnFocus method, IOleControlSite.OnFocus, IOleControlSite::OnFocus, OnFocus, OnFocus method [COM], OnFocus method [COM],IOleControlSite interface, _ctrl_iolecontrolsite_onfocus, com.iolecontrolsite_onfocus, ocidl/IOleControlSite::OnFocus
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
 - IOleControlSite::OnFocus
 - ocidl/IOleControlSite::OnFocus
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
 - IOleControlSite.OnFocus
---

# IOleControlSite::OnFocus


## -description

Indicates whether the control managed by this control site has gained or lost the focus.

## -parameters

### -param fGotFocus [in]

Indicates whether the control gained (TRUE) or lost the focus (FALSE).

## -returns

This method returns S_OK in all cases.

## -remarks

The container uses this information to update the state of <b>Default</b> and <b>Cancel</b> buttons according to how the control with the focus processes Return or Esc keys. A control's behavior regarding the Return and Esc keys is specified in the control's <a href="/windows/desktop/api/ocidl/ns-ocidl-controlinfo">CONTROLINFO</a> structure. See <a href="/windows/desktop/api/ocidl/nf-ocidl-iolecontrol-getcontrolinfo">IOleControl::GetControlInfo</a> for more information.

## -see-also

<a href="/windows/desktop/api/ocidl/nf-ocidl-iolecontrol-getcontrolinfo">IOleControl::GetControlInfo</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-iolecontrolsite">IOleControlSite</a>