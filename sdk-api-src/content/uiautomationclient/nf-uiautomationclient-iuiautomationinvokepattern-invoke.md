---
UID: NF:uiautomationclient.IUIAutomationInvokePattern.Invoke
title: IUIAutomationInvokePattern::Invoke (uiautomationclient.h)
description: Invokes the action of a control, such as a button click.
helpviewer_keywords: ["IUIAutomationInvokePattern interface [Windows Accessibility]","Invoke method","IUIAutomationInvokePattern.Invoke","IUIAutomationInvokePattern::Invoke","Invoke","Invoke method [Windows Accessibility]","Invoke method [Windows Accessibility]","IUIAutomationInvokePattern interface","uiauto.uiauto_IUIAutomationInvokePattern_Invoke","uiauto_IUIAutomationInvokePattern_Invoke","uiautomationclient/IUIAutomationInvokePattern::Invoke","winauto.uiauto_IUIAutomationInvokePattern_Invoke"]
old-location: winauto\uiauto_IUIAutomationInvokePattern_Invoke.htm
tech.root: WinAuto
ms.assetid: dd04426c-edc5-4ee9-95ac-22f32fb14daa
ms.date: 12/05/2018
ms.keywords: IUIAutomationInvokePattern interface [Windows Accessibility],Invoke method, IUIAutomationInvokePattern.Invoke, IUIAutomationInvokePattern::Invoke, Invoke, Invoke method [Windows Accessibility], Invoke method [Windows Accessibility],IUIAutomationInvokePattern interface, uiauto.uiauto_IUIAutomationInvokePattern_Invoke, uiauto_IUIAutomationInvokePattern_Invoke, uiautomationclient/IUIAutomationInvokePattern::Invoke, winauto.uiauto_IUIAutomationInvokePattern_Invoke
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
 - IUIAutomationInvokePattern::Invoke
 - uiautomationclient/IUIAutomationInvokePattern::Invoke
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
 - IUIAutomationInvokePattern.Invoke
---

# IUIAutomationInvokePattern::Invoke


## -description

Invokes the action of a control, such as a button click.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Calls to this method should return immediately without blocking. However, this behavior depends on the implementation.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationinvokepattern">IUIAutomationInvokePattern</a>
