---
UID: NF:uiautomationclient.IUIAutomationMultipleViewPattern.GetCurrentSupportedViews
title: IUIAutomationMultipleViewPattern::GetCurrentSupportedViews (uiautomationclient.h)
description: Retrieves a collection of control-specific view identifiers.
helpviewer_keywords: ["GetCurrentSupportedViews","GetCurrentSupportedViews method [Windows Accessibility]","GetCurrentSupportedViews method [Windows Accessibility]","IUIAutomationMultipleViewPattern interface","IUIAutomationMultipleViewPattern interface [Windows Accessibility]","GetCurrentSupportedViews method","IUIAutomationMultipleViewPattern.GetCurrentSupportedViews","IUIAutomationMultipleViewPattern::GetCurrentSupportedViews","uiauto.uiauto_IUIAutomationMultipleViewPattern_GetCurrentSupportedViews","uiauto_IUIAutomationMultipleViewPattern_GetCurrentSupportedViews","uiautomationclient/IUIAutomationMultipleViewPattern::GetCurrentSupportedViews","winauto.uiauto_IUIAutomationMultipleViewPattern_GetCurrentSupportedViews"]
old-location: winauto\uiauto_IUIAutomationMultipleViewPattern_GetCurrentSupportedViews.htm
tech.root: WinAuto
ms.assetid: 9380797a-b546-4e36-9403-d34cea672ace
ms.date: 12/05/2018
ms.keywords: GetCurrentSupportedViews, GetCurrentSupportedViews method [Windows Accessibility], GetCurrentSupportedViews method [Windows Accessibility],IUIAutomationMultipleViewPattern interface, IUIAutomationMultipleViewPattern interface [Windows Accessibility],GetCurrentSupportedViews method, IUIAutomationMultipleViewPattern.GetCurrentSupportedViews, IUIAutomationMultipleViewPattern::GetCurrentSupportedViews, uiauto.uiauto_IUIAutomationMultipleViewPattern_GetCurrentSupportedViews, uiauto_IUIAutomationMultipleViewPattern_GetCurrentSupportedViews, uiautomationclient/IUIAutomationMultipleViewPattern::GetCurrentSupportedViews, winauto.uiauto_IUIAutomationMultipleViewPattern_GetCurrentSupportedViews
f1_keywords:
- uiautomationclient/IUIAutomationMultipleViewPattern.GetCurrentSupportedViews
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- UIAutomationClient.h
api_name:
- IUIAutomationMultipleViewPattern.GetCurrentSupportedViews
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomationMultipleViewPattern::GetCurrentSupportedViews


## -description


Retrieves a collection of control-specific view identifiers.


## -parameters




### -param retVal [out, retval]

Type: <b><a href="/windows/win32/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a>**</b>

Receives a pointer to an array of view identifiers.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-workingwithsafearrays">Best Practices for Using Safe Arrays</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationmultipleviewpattern">IUIAutomationMultipleViewPattern</a>
 

 

