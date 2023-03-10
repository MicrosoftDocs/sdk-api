---
UID: NN:uiautomationcore.IGridItemProvider
title: IGridItemProvider (uiautomationcore.h)
description: Provides access to individual child controls of containers that implement IGridProvider.
helpviewer_keywords: ["IGridItemProvider","IGridItemProvider interface [Windows Accessibility]","IGridItemProvider interface [Windows Accessibility]","described","uiauto.uiauto_IGridItemProvider","uiauto_IGridItemProvider","uiautomationcore/IGridItemProvider","winauto.uiauto_IGridItemProvider"]
old-location: winauto\uiauto_IGridItemProvider.htm
tech.root: WinAuto
ms.assetid: 334a10f1-8bfc-4935-9eee-6176a3e8a4f1
ms.date: 12/05/2018
ms.keywords: IGridItemProvider, IGridItemProvider interface [Windows Accessibility], IGridItemProvider interface [Windows Accessibility],described, uiauto.uiauto_IGridItemProvider, uiauto_IGridItemProvider, uiautomationcore/IGridItemProvider, winauto.uiauto_IGridItemProvider
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
 - IGridItemProvider
 - uiautomationcore/IGridItemProvider
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
 - IGridItemProvider
---

# IGridItemProvider interface


## -description

Provides access 
        to individual child controls of containers that implement <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-igridprovider">IGridProvider</a>.

## -remarks

Implemented on a UI Automation provider that must support the <a href="/windows/desktop/WinAuto/uiauto-implementinggriditem">GridItem</a> <i>control pattern</i>.
   			

Controls that implement <b>IGridItemProvider</b> can typically be traversed 
            (that is, a UI Automation client can move to adjacent controls) by using the keyboard.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>