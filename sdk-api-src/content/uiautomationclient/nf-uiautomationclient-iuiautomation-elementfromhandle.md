---
UID: NF:uiautomationclient.IUIAutomation.ElementFromHandle
title: IUIAutomation::ElementFromHandle (uiautomationclient.h)
description: Retrieves a UI Automation element for the specified window.
helpviewer_keywords: ["ElementFromHandle","ElementFromHandle method [Windows Accessibility]","ElementFromHandle method [Windows Accessibility]","IUIAutomation interface","IUIAutomation interface [Windows Accessibility]","ElementFromHandle method","IUIAutomation.ElementFromHandle","IUIAutomation::ElementFromHandle","uiauto.uiauto_IUIAutomation_ElementFromHandle","uiauto_IUIAutomation_ElementFromHandle","uiautomationclient/IUIAutomation::ElementFromHandle","winauto.uiauto_IUIAutomation_ElementFromHandle"]
old-location: winauto\uiauto_IUIAutomation_ElementFromHandle.htm
tech.root: WinAuto
ms.assetid: 07c6b7fa-80af-44c2-abcf-a167385892d5
ms.date: 12/05/2018
ms.keywords: ElementFromHandle, ElementFromHandle method [Windows Accessibility], ElementFromHandle method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],ElementFromHandle method, IUIAutomation.ElementFromHandle, IUIAutomation::ElementFromHandle, uiauto.uiauto_IUIAutomation_ElementFromHandle, uiauto_IUIAutomation_ElementFromHandle, uiautomationclient/IUIAutomation::ElementFromHandle, winauto.uiauto_IUIAutomation_ElementFromHandle
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAutomation::ElementFromHandle
 - uiautomationclient/IUIAutomation::ElementFromHandle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomation.ElementFromHandle
---

# IUIAutomation::ElementFromHandle


## -description

Retrieves a UI Automation element for the specified window.

## -parameters

### -param hwnd [in]

Type: <b>UIA_HWND</b>

The window handle.

### -param element [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>**</b>

Receives a pointer to the element.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation">IUIAutomation</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-elementfromhandlebuildcache">IUIAutomation::ElementFromHandleBuildCache</a>