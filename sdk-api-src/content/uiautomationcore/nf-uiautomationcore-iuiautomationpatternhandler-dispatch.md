---
UID: NF:uiautomationcore.IUIAutomationPatternHandler.Dispatch
title: IUIAutomationPatternHandler::Dispatch (uiautomationcore.h)
description: Dispatches a method or property getter to a custom control pattern provider.
helpviewer_keywords: ["Dispatch","Dispatch method [Windows Accessibility]","Dispatch method [Windows Accessibility]","IUIAutomationPatternHandler interface","IUIAutomationPatternHandler interface [Windows Accessibility]","Dispatch method","IUIAutomationPatternHandler.Dispatch","IUIAutomationPatternHandler::Dispatch","uiauto.uiauto_IUIAutomationPatternHandler_Dispatch","uiauto_IUIAutomationPatternHandler_Dispatch","uiautomationcore/IUIAutomationPatternHandler::Dispatch","winauto.uiauto_IUIAutomationPatternHandler_Dispatch"]
old-location: winauto\uiauto_IUIAutomationPatternHandler_Dispatch.htm
tech.root: WinAuto
ms.assetid: c94d650e-74a8-4d4f-92bf-5402576f8773
ms.date: 12/05/2018
ms.keywords: Dispatch, Dispatch method [Windows Accessibility], Dispatch method [Windows Accessibility],IUIAutomationPatternHandler interface, IUIAutomationPatternHandler interface [Windows Accessibility],Dispatch method, IUIAutomationPatternHandler.Dispatch, IUIAutomationPatternHandler::Dispatch, uiauto.uiauto_IUIAutomationPatternHandler_Dispatch, uiauto_IUIAutomationPatternHandler_Dispatch, uiautomationcore/IUIAutomationPatternHandler::Dispatch, winauto.uiauto_IUIAutomationPatternHandler_Dispatch
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
 - IUIAutomationPatternHandler::Dispatch
 - uiautomationcore/IUIAutomationPatternHandler::Dispatch
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
 - IUIAutomationPatternHandler.Dispatch
---

# IUIAutomationPatternHandler::Dispatch


## -description

Dispatches a method or property getter to a custom <i>control pattern</i> provider.

## -parameters

### -param pTarget [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to the object that implements the control pattern provider.

### -param index [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The index of the method or property getter.

### -param pParams [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/ns-uiautomationcore-uiautomationparameter">UIAutomationParameter</a>*</b>

A pointer to an array of structures that contain information about the parameters to be passed.

### -param cParams [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The count of parameters in <i>pParams</i>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iuiautomationpatternhandler">IUIAutomationPatternHandler</a>