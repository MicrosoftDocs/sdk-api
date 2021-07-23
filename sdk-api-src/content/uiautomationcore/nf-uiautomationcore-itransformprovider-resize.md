---
UID: NF:uiautomationcore.ITransformProvider.Resize
title: ITransformProvider::Resize (uiautomationcore.h)
description: Resizes the control.
helpviewer_keywords: ["ITransformProvider interface [Windows Accessibility]","Resize method","ITransformProvider.Resize","ITransformProvider::Resize","Resize","Resize method [Windows Accessibility]","Resize method [Windows Accessibility]","ITransformProvider interface","uiauto.uiauto_ITransformProvider_Resize","uiauto_ITransformProvider_Resize","uiautomationcore/ITransformProvider::Resize","winauto.uiauto_ITransformProvider_Resize"]
old-location: winauto\uiauto_ITransformProvider_Resize.htm
tech.root: WinAuto
ms.assetid: ba22f770-1306-4c15-bc72-a928b91e0eb5
ms.date: 12/05/2018
ms.keywords: ITransformProvider interface [Windows Accessibility],Resize method, ITransformProvider.Resize, ITransformProvider::Resize, Resize, Resize method [Windows Accessibility], Resize method [Windows Accessibility],ITransformProvider interface, uiauto.uiauto_ITransformProvider_Resize, uiauto_ITransformProvider_Resize, uiautomationcore/ITransformProvider::Resize, winauto.uiauto_ITransformProvider_Resize
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
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
 - ITransformProvider::Resize
 - uiautomationcore/ITransformProvider::Resize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.h
api_name:
 - ITransformProvider.Resize
---

# ITransformProvider::Resize


## -description

Resizes the control.

## -parameters

### -param width [in]

Type: <b>double</b>

The new width of the window in pixels.

### -param height [in]

Type: <b>double</b>

The new height of the window in pixels.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When called on a control supporting split panes, this method might have the 
            side effect of resizing other contiguous panes. 
            

An object cannot be moved, resized, or rotated such that its resulting screen location 
            would be completely outside the coordinates of its container and inaccessible to keyboard 
            or mouse. For example, a top-level window moved completely off-screen or a child object 
            moved outside the boundaries of the container's viewport. In these cases the object is 
            placed as close to the requested screen coordinates as possible with the top or left 
            coordinates overridden to be within the container boundaries.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itransformprovider">ITransformProvider</a>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>