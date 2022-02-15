---
UID: NN:uiautomationclient.IUIAutomation
title: IUIAutomation (uiautomationclient.h)
description: Exposes methods that enable Microsoft UI Automation client applications to discover, access, and filter UI Automation elements.
helpviewer_keywords: ["IUIAutomation","IUIAutomation interface [Windows Accessibility]","IUIAutomation interface [Windows Accessibility]","described","uiauto.uiauto_IUIAutomation","uiauto_IUIAutomation","uiautomationclient/IUIAutomation","winauto.uiauto_IUIAutomation"]
old-location: winauto\uiauto_IUIAutomation.htm
tech.root: WinAuto
ms.assetid: 46b31ab6-39aa-4df8-a421-6369c32a9605
ms.date: 12/05/2018
ms.keywords: IUIAutomation, IUIAutomation interface [Windows Accessibility], IUIAutomation interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomation, uiauto_IUIAutomation, uiautomationclient/IUIAutomation, winauto.uiauto_IUIAutomation
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
req.dll: UIAutomationCore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAutomation
 - uiautomationclient/IUIAutomation
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
 - IUIAutomation
---

# IUIAutomation interface


## -description

Exposes methods that enable Microsoft UI Automation client applications to discover, access, and filter UI Automation elements. UI Automation exposes every element of the UI Automation as an object represented by the <b>IUIAutomation</b> interface. The members of this interface are not specific to a particular element.

## -inheritance

The <b>IUIAutomation</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAutomation</b> also has these types of members:

## -remarks

Every UI Automation client application must obtain this interface to a <a href="/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)">CUIAutomation</a> object in order to gain access to the functionality of UI Automation.
	        

The following example function creates a <a href="/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)">CUIAutomation</a> object and obtains the <b>IUIAutomation</b> interface.



```
IUIAutomation *g_pAutomation;

BOOL InitializeUIAutomation()
{
    CoInitialize(NULL);
    HRESULT hr = CoCreateInstance(__uuidof(CUIAutomation), NULL, CLSCTX_INPROC_SERVER, 
        __uuidof(IUIAutomation), (void**)&g_pAutomation);
    return (SUCCEEDED(hr));
}
```

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-entry-uiautoclientinterfaces">UI Automation Element Interfaces for Clients</a>
