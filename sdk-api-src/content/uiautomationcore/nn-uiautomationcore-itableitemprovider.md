---
UID: NN:uiautomationcore.ITableItemProvider
title: ITableItemProvider (uiautomationcore.h)
description: Provides access to child controls of containers that implement ITableProvider.
helpviewer_keywords: ["ITableItemProvider","ITableItemProvider interface [Windows Accessibility]","ITableItemProvider interface [Windows Accessibility]","described","uiauto.uiauto_ITableItemProvider","uiauto_ITableItemProvider","uiautomationcore/ITableItemProvider","winauto.uiauto_ITableItemProvider"]
old-location: winauto\uiauto_ITableItemProvider.htm
tech.root: WinAuto
ms.assetid: 73cba491-1aa6-4bd7-bcd6-95b5d85c9457
ms.date: 12/05/2018
ms.keywords: ITableItemProvider, ITableItemProvider interface [Windows Accessibility], ITableItemProvider interface [Windows Accessibility],described, uiauto.uiauto_ITableItemProvider, uiauto_ITableItemProvider, uiautomationcore/ITableItemProvider, winauto.uiauto_ITableItemProvider
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
 - ITableItemProvider
 - uiautomationcore/ITableItemProvider
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
 - ITableItemProvider
---

# ITableItemProvider interface


## -description

Provides access 
        to child controls of containers that implement <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itableprovider">ITableProvider</a>.

## -inheritance

The <b>ITableItemProvider</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITableItemProvider</b> also has these types of members:

## -remarks

This control pattern is analogous to <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-igriditemprovider">IGridItemProvider</a> with 
            the distinction that any control implementing <b>ITableItemProvider</b> 
            must expose the relationship between the individual cell and its row and column information.
            

Access to individual cell functionality is provided by the concurrent implementation 
            of <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-igriditemprovider">IGridItemProvider</a>. 
            

Implemented on a UI Automation provider that must 
            support the <a href="/windows/desktop/WinAuto/uiauto-implementingtableitem">TableItem</a> control pattern.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>
