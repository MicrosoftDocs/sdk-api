---
UID: NN:uiautomationcore.IValueProvider
title: IValueProvider (uiautomationcore.h)
description: Provides access to controls that have an intrinsic value that does not span a range, and that can be represented as a string.
helpviewer_keywords: ["IValueProvider","IValueProvider interface [Windows Accessibility]","IValueProvider interface [Windows Accessibility]","described","uiauto.uiauto_IValueProvider","uiauto_IValueProvider","uiautomationcore/IValueProvider","winauto.uiauto_IValueProvider"]
old-location: winauto\uiauto_IValueProvider.htm
tech.root: WinAuto
ms.assetid: e6adbc23-dbfe-4dd2-82d9-66ce16de3338
ms.date: 12/05/2018
ms.keywords: IValueProvider, IValueProvider interface [Windows Accessibility], IValueProvider interface [Windows Accessibility],described, uiauto.uiauto_IValueProvider, uiauto_IValueProvider, uiautomationcore/IValueProvider, winauto.uiauto_IValueProvider
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
 - IValueProvider
 - uiautomationcore/IValueProvider
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
 - IValueProvider
---

# IValueProvider interface


## -description

Provides access 
        to controls that have an intrinsic value that does not span a range, and that can be represented as a string.

## -inheritance

The <b>IValueProvider</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IValueProvider</b> also has these types of members:

## -remarks

The value of the control may or may not be editable depending on the control and its settings.
        

Implemented on a Microsoft UI Automation provider that must support the <a href="/windows/desktop/WinAuto/uiauto-implementingvalue">Value</a> control pattern.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>
