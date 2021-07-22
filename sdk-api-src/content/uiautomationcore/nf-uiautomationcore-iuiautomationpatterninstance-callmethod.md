---
UID: NF:uiautomationcore.IUIAutomationPatternInstance.CallMethod
title: IUIAutomationPatternInstance::CallMethod (uiautomationcore.h)
description: Client wrapper implements methods by calling this CallMethod function, specifying the parameters as an array of pointers.
helpviewer_keywords: ["CallMethod","CallMethod method [Windows Accessibility]","CallMethod method [Windows Accessibility]","IUIAutomationPatternInstance interface","IUIAutomationPatternInstance interface [Windows Accessibility]","CallMethod method","IUIAutomationPatternInstance.CallMethod","IUIAutomationPatternInstance::CallMethod","uiauto.uiauto_IUIAutomationPatternInstance_CallMethod","uiauto_IUIAutomationPatternInstance_CallMethod","uiautomationcore/IUIAutomationPatternInstance::CallMethod","winauto.uiauto_IUIAutomationPatternInstance_CallMethod"]
old-location: winauto\uiauto_IUIAutomationPatternInstance_CallMethod.htm
tech.root: WinAuto
ms.assetid: a3c1aa20-c512-4752-8da6-c8e86bd56beb
ms.date: 12/05/2018
ms.keywords: CallMethod, CallMethod method [Windows Accessibility], CallMethod method [Windows Accessibility],IUIAutomationPatternInstance interface, IUIAutomationPatternInstance interface [Windows Accessibility],CallMethod method, IUIAutomationPatternInstance.CallMethod, IUIAutomationPatternInstance::CallMethod, uiauto.uiauto_IUIAutomationPatternInstance_CallMethod, uiauto_IUIAutomationPatternInstance_CallMethod, uiautomationcore/IUIAutomationPatternInstance::CallMethod, winauto.uiauto_IUIAutomationPatternInstance_CallMethod
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
 - IUIAutomationPatternInstance::CallMethod
 - uiautomationcore/IUIAutomationPatternInstance::CallMethod
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
 - IUIAutomationPatternInstance.CallMethod
---

# IUIAutomationPatternInstance::CallMethod


## -description

Client wrapper implements methods by calling this CallMethod function, specifying the parameters as an array of pointers.

## -parameters

### -param index [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The index of the method.

### -param pParams [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/ns-uiautomationcore-uiautomationparameter">UIAutomationParameter</a>*</b>

 A pointer to an array of structures describing the parameters.

### -param cParams [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The count of parameters in <i>pParams</i>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iuiautomationpatterninstance">IUIAutomationPatternInstance</a>