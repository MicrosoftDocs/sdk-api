---
UID: NN:uiautomationcore.ITransformProvider
title: ITransformProvider (uiautomationcore.h)
description: Provides access to controls that can be moved, resized, and/or rotated within a two-dimensional space.
helpviewer_keywords: ["ITransformProvider","ITransformProvider interface [Windows Accessibility]","ITransformProvider interface [Windows Accessibility]","described","uiauto.uiauto_ITransformProvider","uiauto_ITransformProvider","uiautomationcore/ITransformProvider","winauto.uiauto_ITransformProvider"]
old-location: winauto\uiauto_ITransformProvider.htm
tech.root: WinAuto
ms.assetid: cdc2f81b-cf69-469f-9139-e9a73cf8c730
ms.date: 12/05/2018
ms.keywords: ITransformProvider, ITransformProvider interface [Windows Accessibility], ITransformProvider interface [Windows Accessibility],described, uiauto.uiauto_ITransformProvider, uiauto_ITransformProvider, uiautomationcore/ITransformProvider, winauto.uiauto_ITransformProvider
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
 - ITransformProvider
 - uiautomationcore/ITransformProvider
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
 - ITransformProvider
---

# ITransformProvider interface


## -description

Provides access 
        to controls that can be moved, resized, and/or rotated within a two-dimensional space.

## -inheritance

The <b>ITransformProvider</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITransformProvider</b> also has these types of members:

## -remarks

Implemented on a Microsoft UI Automation provider that must support the <a href="/windows/desktop/WinAuto/uiauto-implementingtransform">Transform</a> control pattern.
            

Support for this  control pattern is not limited to objects on the desktop. 
            This  control pattern must also be implemented by the children of a 
            container object as long as the children can be moved, resized, or rotated freely within the boundaries of the container.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itransformprovider2">ITransformProvider2</a>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>
