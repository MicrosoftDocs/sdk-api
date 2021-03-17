---
UID: NN:uiautomationcore.ITextChildProvider
title: ITextChildProvider (uiautomationcore.h)
description: Provides access to a text-based control (or an object embedded in text) that is a child or descendant of another text-based control.
helpviewer_keywords: ["ITextChildProvider","ITextChildProvider interface [Windows Accessibility]","ITextChildProvider interface [Windows Accessibility]","described","uiautomationcore/ITextChildProvider","winauto.uiauto__ITextChildProvider"]
old-location: winauto\uiauto__ITextChildProvider.htm
tech.root: WinAuto
ms.assetid: 370A772A-0AD9-4183-B316-CADC4FE117AE
ms.date: 12/05/2018
ms.keywords: ITextChildProvider, ITextChildProvider interface [Windows Accessibility], ITextChildProvider interface [Windows Accessibility],described, uiautomationcore/ITextChildProvider, winauto.uiauto__ITextChildProvider
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - ITextChildProvider
 - uiautomationcore/ITextChildProvider
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
 - ITextChildProvider
---

# ITextChildProvider interface


## -description

Provides access to a text-based control (or an object embedded in text) that is a child or descendant of another text-based control.

## -remarks

An element that implements the [TextChild control pattern](/windows/desktop/WinAuto/textchild-control-pattern) must be a child, or descendent, of an element that supports the [Text control pattern](/windows/desktop/WinAuto/uiauto-implementingtextandtextrange).

It is not required that this element also implement the [Text control pattern](/windows/desktop/WinAuto/uiauto-implementingtextandtextrange).

## -see-also

[Text control pattern](/windows/desktop/WinAuto/uiauto-implementingtextandtextrange), [TextChild control pattern](/windows/desktop/WinAuto/textchild-control-pattern), [UI Automation Providers Overview](/windows/desktop/WinAuto/uiauto-providersoverview)