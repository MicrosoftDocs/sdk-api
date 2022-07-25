---
UID: NF:uiautomationclient.IUIAutomationTransformPattern.Move
title: IUIAutomationTransformPattern::Move (uiautomationclient.h)
description: Moves the UI Automation element.
helpviewer_keywords: ["IUIAutomationTransformPattern interface [Windows Accessibility]","Move method","IUIAutomationTransformPattern.Move","IUIAutomationTransformPattern::Move","Move","Move method [Windows Accessibility]","Move method [Windows Accessibility]","IUIAutomationTransformPattern interface","uiauto.uiauto_IUIAutomationTransformPattern_Move","uiauto_IUIAutomationTransformPattern_Move","uiautomationclient/IUIAutomationTransformPattern::Move","winauto.uiauto_IUIAutomationTransformPattern_Move"]
old-location: winauto\uiauto_IUIAutomationTransformPattern_Move.htm
tech.root: WinAuto
ms.assetid: 6529de7b-cb7d-4e18-b274-bc6bf003f912
ms.date: 12/05/2018
ms.keywords: IUIAutomationTransformPattern interface [Windows Accessibility],Move method, IUIAutomationTransformPattern.Move, IUIAutomationTransformPattern::Move, Move, Move method [Windows Accessibility], Move method [Windows Accessibility],IUIAutomationTransformPattern interface, uiauto.uiauto_IUIAutomationTransformPattern_Move, uiauto_IUIAutomationTransformPattern_Move, uiautomationclient/IUIAutomationTransformPattern::Move, winauto.uiauto_IUIAutomationTransformPattern_Move
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationClient.idl
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
 - IUIAutomationTransformPattern::Move
 - uiautomationclient/IUIAutomationTransformPattern::Move
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomationTransformPattern.Move
---

# IUIAutomationTransformPattern::Move


## -description

Moves the UI Automation element.

## -parameters

### -param x [in]

Type: <b>double</b>

Absolute screen coordinates of the left side of the control.

### -param y [in]

Type: <b>double</b>

Absolute screen coordinates of the top of the control.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

An element cannot be moved, resized or rotated such that its resulting screen location would be completely outside the coordinates of its container and inaccessible to the keyboard or mouse. For example, when a top-level window is moved completely off-screen or a child object is moved outside the boundaries of the container's viewport, the object is placed as close to the requested screen coordinates as possible with the top or left coordinates overridden to be within the container boundaries.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtransformpattern-get_cachedcanmove">CachedCanMove</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtransformpattern-get_currentcanmove">CurrentCanMove</a>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtransformpattern">IUIAutomationTransformPattern</a>