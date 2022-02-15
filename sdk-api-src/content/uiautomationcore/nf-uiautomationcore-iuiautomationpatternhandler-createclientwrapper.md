---
UID: NF:uiautomationcore.IUIAutomationPatternHandler.CreateClientWrapper
title: IUIAutomationPatternHandler::CreateClientWrapper (uiautomationcore.h)
description: Creates an object that enables a client application to interact with a custom control pattern.
helpviewer_keywords: ["CreateClientWrapper","CreateClientWrapper method [Windows Accessibility]","CreateClientWrapper method [Windows Accessibility]","IUIAutomationPatternHandler interface","IUIAutomationPatternHandler interface [Windows Accessibility]","CreateClientWrapper method","IUIAutomationPatternHandler.CreateClientWrapper","IUIAutomationPatternHandler::CreateClientWrapper","uiauto.uiauto_IUIAutomationPatternHandler_CreateClientWrapper","uiauto_IUIAutomationPatternHandler_CreateClientWrapper","uiautomationcore/IUIAutomationPatternHandler::CreateClientWrapper","winauto.uiauto_IUIAutomationPatternHandler_CreateClientWrapper"]
old-location: winauto\uiauto_IUIAutomationPatternHandler_CreateClientWrapper.htm
tech.root: WinAuto
ms.assetid: 03530381-52f8-4d9b-a54c-faebf7cd4a06
ms.date: 12/05/2018
ms.keywords: CreateClientWrapper, CreateClientWrapper method [Windows Accessibility], CreateClientWrapper method [Windows Accessibility],IUIAutomationPatternHandler interface, IUIAutomationPatternHandler interface [Windows Accessibility],CreateClientWrapper method, IUIAutomationPatternHandler.CreateClientWrapper, IUIAutomationPatternHandler::CreateClientWrapper, uiauto.uiauto_IUIAutomationPatternHandler_CreateClientWrapper, uiauto_IUIAutomationPatternHandler_CreateClientWrapper, uiautomationcore/IUIAutomationPatternHandler::CreateClientWrapper, winauto.uiauto_IUIAutomationPatternHandler_CreateClientWrapper
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAutomationPatternHandler::CreateClientWrapper
 - uiautomationcore/IUIAutomationPatternHandler::CreateClientWrapper
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.h
api_name:
 - IUIAutomationPatternHandler.CreateClientWrapper
---

# IUIAutomationPatternHandler::CreateClientWrapper


## -description

Creates an object that enables a client application to interact with a custom <i>control pattern</i>.

## -parameters

### -param pPatternInstance [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iuiautomationpatterninstance">IUIAutomationPatternInstance</a>*</b>

A pointer to the instance of the control pattern that will be used by the wrapper.

### -param pClientWrapper [out, retval]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>**</b>

Receives a pointer to the wrapper object.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The wrapper object exposes methods and properties of the <i>control pattern</i>. The implementation of the wrapper class passes these calls to Microsoft UI Automation by calling <a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iuiautomationpatterninstance-callmethod">CallMethod</a> and <a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iuiautomationpatterninstance-getproperty">GetProperty</a>.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iuiautomationpatternhandler">IUIAutomationPatternHandler</a>