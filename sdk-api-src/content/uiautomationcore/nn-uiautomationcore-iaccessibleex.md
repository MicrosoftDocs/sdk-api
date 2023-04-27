---
UID: NN:uiautomationcore.IAccessibleEx
title: IAccessibleEx (uiautomationcore.h)
description: Exposes methods that are called by Microsoft UI Automation to retrieve extra information about a control that supports Microsoft Active Accessibility.
helpviewer_keywords: ["IAccessibleEx","IAccessibleEx interface [Windows Accessibility]","IAccessibleEx interface [Windows Accessibility]","described","uiauto.uiauto_IAccessibleEx","uiauto_IAccessibleEx","uiautomationcore/IAccessibleEx","winauto.uiauto_IAccessibleEx"]
old-location: winauto\uiauto_IAccessibleEx.htm
tech.root: WinAuto
ms.assetid: 90211503-a73c-4380-be96-0be40ad29382
ms.date: 12/05/2018
ms.keywords: IAccessibleEx, IAccessibleEx interface [Windows Accessibility], IAccessibleEx interface [Windows Accessibility],described, uiauto.uiauto_IAccessibleEx, uiauto_IAccessibleEx, uiautomationcore/IAccessibleEx, winauto.uiauto_IAccessibleEx
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
 - IAccessibleEx
 - uiautomationcore/IAccessibleEx
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
 - IAccessibleEx
---

# IAccessibleEx interface


## -description

Exposes methods that are called by [Microsoft UI Automation](/windows/win32/winauto/entry-uiauto-win32) to retrieve extra information about a control that supports [Microsoft Active Accessibility](/windows/win32/winauto/microsoft-active-accessibility).

## -inheritance

The **IAccessibleEx** interface inherits from the [IUnknown](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface. **IAccessibleEx** also has these types of members:

## -remarks

This interface can be implemented on custom controls that also implement the [IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface, to provide added support for UI Automation without the cost of a full UI Automation provider implementation.

## -see-also

[Adding UI Automation Functionality to Active Accessibility Servers](/windows/desktop/WinAuto/uiauto-usingiaccessibleex)
