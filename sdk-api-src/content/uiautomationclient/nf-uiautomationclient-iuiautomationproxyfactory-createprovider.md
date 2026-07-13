---
UID: NF:uiautomationclient.IUIAutomationProxyFactory.CreateProvider
title: IUIAutomationProxyFactory::CreateProvider (uiautomationclient.h)
description: Creates a proxy object that provides Microsoft UI Automation support for a UI element.
helpviewer_keywords: ["CreateProvider","CreateProvider method [Windows Accessibility]","CreateProvider method [Windows Accessibility]","IUIAutomationProxyFactory interface","IUIAutomationProxyFactory interface [Windows Accessibility]","CreateProvider method","IUIAutomationProxyFactory.CreateProvider","IUIAutomationProxyFactory::CreateProvider","uiauto.uiauto_IUIAutomationProxyFactory_CreateProvider","uiauto_IUIAutomationProxyFactory_CreateProvider","uiautomationclient/IUIAutomationProxyFactory::CreateProvider","winauto.uiauto_IUIAutomationProxyFactory_CreateProvider"]
old-location: winauto\uiauto_IUIAutomationProxyFactory_CreateProvider.htm
tech.root: WinAuto
ms.assetid: c7ac43d3-443f-42cf-98d5-e558034c9d40
ms.date: 12/05/2018
ms.keywords: CreateProvider, CreateProvider method [Windows Accessibility], CreateProvider method [Windows Accessibility],IUIAutomationProxyFactory interface, IUIAutomationProxyFactory interface [Windows Accessibility],CreateProvider method, IUIAutomationProxyFactory.CreateProvider, IUIAutomationProxyFactory::CreateProvider, uiauto.uiauto_IUIAutomationProxyFactory_CreateProvider, uiauto_IUIAutomationProxyFactory_CreateProvider, uiautomationclient/IUIAutomationProxyFactory::CreateProvider, winauto.uiauto_IUIAutomationProxyFactory_CreateProvider
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
 - IUIAutomationProxyFactory::CreateProvider
 - uiautomationclient/IUIAutomationProxyFactory::CreateProvider
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
 - IUIAutomationProxyFactory.CreateProvider
---

# IUIAutomationProxyFactory::CreateProvider


## -description

Creates a proxy object that provides Microsoft UI Automation support for a UI element.

## -parameters

### -param hwnd [in]

Type: <b>UIA_HWND</b>

The window handle of the UI element.

### -param idObject [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a></b>

The object ID. See Remarks.

### -param idChild [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a></b>

The child ID. See Remarks.

### -param provider [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementprovidersimple">IRawElementProviderSimple</a>**</b>

Receives a pointer to the proxy object.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <i>idObject</i> parameter is normally <a href="/windows/desktop/WinAuto/object-identifiers">OBJID_CLIENT</a>, and <i>idChild</i> is normally CHILDID_SELF. However, when the method is called in response to a registered WinEvent, these values are from the event, specifying the subelement that raised the event.