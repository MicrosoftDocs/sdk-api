---
UID: NN:uiautomationcore.IGridProvider
title: IGridProvider (uiautomationcore.h)
description: Provides access to controls that act as containers for a collection of child elements organized in a two-dimensional logical coordinate system that can be traversed (that is, a Microsoft UI Automation client can move to adjacent controls) by using the keyboard.
helpviewer_keywords: ["IGridProvider","IGridProvider interface [Windows Accessibility]","IGridProvider interface [Windows Accessibility]","described","uiauto.uiauto_IGridProvider","uiauto_IGridProvider","uiautomationcore/IGridProvider","winauto.uiauto_IGridProvider"]
old-location: winauto\uiauto_IGridProvider.htm
tech.root: WinAuto
ms.assetid: 37e2cc95-d765-4c2c-ae8a-5a072a43ad5a
ms.date: 12/05/2018
ms.keywords: IGridProvider, IGridProvider interface [Windows Accessibility], IGridProvider interface [Windows Accessibility],described, uiauto.uiauto_IGridProvider, uiauto_IGridProvider, uiautomationcore/IGridProvider, winauto.uiauto_IGridProvider
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
req.dll: UIAutomationCore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGridProvider
 - uiautomationcore/IGridProvider
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.dll
api_name:
 - IGridProvider
---

# IGridProvider interface


## -description

Provides access to 
        controls that act as containers for a collection of child elements organized in a two-dimensional 
        logical coordinate system that can be traversed (that is, a Microsoft UI Automation client can 
        move to adjacent controls) by using the keyboard. The children of this 
        element must implement <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-igriditemprovider">IGridItemProvider</a>.

## -inheritance

The <b>IGridProvider</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IGridProvider</b> also has these types of members:

## -remarks

The <b>IGridProvider</b> interface exposes methods and properties to support UI Automation client access to controls 
		that act as containers for a collection of child elements. The children of this element must implement <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-igriditemprovider">IGridItemProvider</a> and be organized in a two-dimensional logical coordinate system that can be traversed (that is, a UI Automation client can move to adjacent controls) by using the keyboard.
		

Implemented on a UI Automation provider that must support 
        the <a href="/windows/desktop/WinAuto/uiauto-implementinggrid">Grid</a> control pattern.

<b>IGridProvider</b> does not enable active manipulation of a grid; 
        <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itransformprovider">ITransformProvider</a> must be implemented for this.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>
