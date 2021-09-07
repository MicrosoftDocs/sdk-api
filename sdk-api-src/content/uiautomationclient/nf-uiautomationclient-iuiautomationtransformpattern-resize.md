---
UID: NF:uiautomationclient.IUIAutomationTransformPattern.Resize
title: IUIAutomationTransformPattern::Resize (uiautomationclient.h)
description: Resizes the UI Automation element.
helpviewer_keywords: ["IUIAutomationTransformPattern interface [Windows Accessibility]","Resize method","IUIAutomationTransformPattern.Resize","IUIAutomationTransformPattern::Resize","Resize","Resize method [Windows Accessibility]","Resize method [Windows Accessibility]","IUIAutomationTransformPattern interface","uiauto.uiauto_IUIAutomationTransformPattern_Resize","uiauto_IUIAutomationTransformPattern_Resize","uiautomationclient/IUIAutomationTransformPattern::Resize","winauto.uiauto_IUIAutomationTransformPattern_Resize"]
old-location: winauto\uiauto_IUIAutomationTransformPattern_Resize.htm
tech.root: WinAuto
ms.assetid: af5611ef-d14c-44c2-8065-7c7581a16198
ms.date: 12/05/2018
ms.keywords: IUIAutomationTransformPattern interface [Windows Accessibility],Resize method, IUIAutomationTransformPattern.Resize, IUIAutomationTransformPattern::Resize, Resize, Resize method [Windows Accessibility], Resize method [Windows Accessibility],IUIAutomationTransformPattern interface, uiauto.uiauto_IUIAutomationTransformPattern_Resize, uiauto_IUIAutomationTransformPattern_Resize, uiautomationclient/IUIAutomationTransformPattern::Resize, winauto.uiauto_IUIAutomationTransformPattern_Resize
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
 - IUIAutomationTransformPattern::Resize
 - uiautomationclient/IUIAutomationTransformPattern::Resize
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
 - IUIAutomationTransformPattern.Resize
---

# IUIAutomationTransformPattern::Resize


## -description

Resizes the UI Automation element.

## -parameters

### -param width [in]

Type: <b>double</b>

The new width of the window, in pixels.

### -param height [in]

Type: <b>double</b>

The new height of the window, in pixels.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When called on a control that supports split panes, this method can have the side effect of resizing other contiguous panes. 

An object cannot be moved, resized, or rotated such that its resulting screen location would be completely outside the coordinates of its container and inaccessible to the keyboard or mouse. For example, when a top-level window is moved completely off-screen or a child object is moved outside the boundaries of the container's viewport. In these cases the object is placed as close to the requested screen coordinates as possible with the top or left coordinates overridden to be within the container boundaries.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtransformpattern-get_cachedcanresize">CachedCanResize</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtransformpattern-get_currentcanresize">CurrentCanResize</a>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtransformpattern">IUIAutomationTransformPattern</a>