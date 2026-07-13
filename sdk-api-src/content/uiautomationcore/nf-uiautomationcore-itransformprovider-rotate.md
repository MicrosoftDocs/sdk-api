---
UID: NF:uiautomationcore.ITransformProvider.Rotate
title: ITransformProvider::Rotate (uiautomationcore.h)
description: Rotates the control.
helpviewer_keywords: ["ITransformProvider interface [Windows Accessibility]","Rotate method","ITransformProvider.Rotate","ITransformProvider::Rotate","Rotate","Rotate method [Windows Accessibility]","Rotate method [Windows Accessibility]","ITransformProvider interface","uiauto.uiauto_ITransformProvider_Rotate","uiauto_ITransformProvider_Rotate","uiautomationcore/ITransformProvider::Rotate","winauto.uiauto_ITransformProvider_Rotate"]
old-location: winauto\uiauto_ITransformProvider_Rotate.htm
tech.root: WinAuto
ms.assetid: 2e8255de-b28d-4fc4-82ea-4255771f9838
ms.date: 12/05/2018
ms.keywords: ITransformProvider interface [Windows Accessibility],Rotate method, ITransformProvider.Rotate, ITransformProvider::Rotate, Rotate, Rotate method [Windows Accessibility], Rotate method [Windows Accessibility],ITransformProvider interface, uiauto.uiauto_ITransformProvider_Rotate, uiauto_ITransformProvider_Rotate, uiautomationcore/ITransformProvider::Rotate, winauto.uiauto_ITransformProvider_Rotate
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
 - ITransformProvider::Rotate
 - uiautomationcore/ITransformProvider::Rotate
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
 - ITransformProvider.Rotate
---

# ITransformProvider::Rotate


## -description

Rotates the control.

## -parameters

### -param degrees [in]

Type: <b>double</b>

The number of degrees to rotate the control. 
				A positive number rotates clockwise; a negative number rotates counterclockwise.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

An object cannot be moved, resized, or rotated such that its resulting screen location 
            would be completely outside the coordinates of its container and inaccessible to keyboard 
            or mouse. For example, a top-level window moved completely off-screen or a child object 
            moved outside the boundaries of the container's viewport. In these cases the object is 
            placed as close to the requested screen coordinates as possible with the top or left 
            coordinates overridden to be within the container boundaries.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itransformprovider">ITransformProvider</a>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>