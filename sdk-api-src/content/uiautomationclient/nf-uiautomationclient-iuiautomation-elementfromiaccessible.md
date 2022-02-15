---
UID: NF:uiautomationclient.IUIAutomation.ElementFromIAccessible
title: IUIAutomation::ElementFromIAccessible (uiautomationclient.h)
description: Retrieves a UI Automation element for the specified accessible object from a Microsoft Active Accessibility server.
helpviewer_keywords: ["ElementFromIAccessible","ElementFromIAccessible method [Windows Accessibility]","ElementFromIAccessible method [Windows Accessibility]","IUIAutomation interface","IUIAutomation interface [Windows Accessibility]","ElementFromIAccessible method","IUIAutomation.ElementFromIAccessible","IUIAutomation::ElementFromIAccessible","uiauto.uiauto_IUIAutomation_ElementFromIAccessible","uiauto_IUIAutomation_ElementFromIAccessible","uiautomationclient/IUIAutomation::ElementFromIAccessible","winauto.uiauto_IUIAutomation_ElementFromIAccessible"]
old-location: winauto\uiauto_IUIAutomation_ElementFromIAccessible.htm
tech.root: WinAuto
ms.assetid: b3dcc31c-e111-4841-82a8-a6329020b595
ms.date: 12/05/2018
ms.keywords: ElementFromIAccessible, ElementFromIAccessible method [Windows Accessibility], ElementFromIAccessible method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],ElementFromIAccessible method, IUIAutomation.ElementFromIAccessible, IUIAutomation::ElementFromIAccessible, uiauto.uiauto_IUIAutomation_ElementFromIAccessible, uiauto_IUIAutomation_ElementFromIAccessible, uiautomationclient/IUIAutomation::ElementFromIAccessible, winauto.uiauto_IUIAutomation_ElementFromIAccessible
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
 - IUIAutomation::ElementFromIAccessible
 - uiautomationclient/IUIAutomation::ElementFromIAccessible
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
 - IUIAutomation.ElementFromIAccessible
---

# IUIAutomation::ElementFromIAccessible


## -description

Retrieves a UI Automation element for the specified accessible object from a Microsoft Active Accessibility server.

## -parameters

### -param accessible [in]

Type: <b><a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a>*</b>

A pointer to the <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> interface of the accessible object.

### -param childId [in]

Type: <b>int</b>

The child ID of the accessible object.

### -param element [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>**</b>

Receives a pointer to the UI Automation element.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method enables UI Automation clients to get <a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a> interfaces for accessible objects implemented by a Microsoft Active Accessibility server. 

This method may fail if the server implements UI Automation provider interfaces alongside Microsoft Active Accessibility support. 

The method returns E_INVALIDARG if the underlying implementation of the Microsoft UI Automation element is not a native Microsoft Active Accessibility server; that is, if a client attempts to retrieve the <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> interface for an element originally supported by a proxy object from Oleacc.dll, or by the UIA-to-MSAA Bridge.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation">IUIAutomation</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-elementfromhandlebuildcache">IUIAutomation::ElementFromHandleBuildCache</a>