---
UID: NF:uiautomationclient.IUIAutomationMultipleViewPattern.GetCachedSupportedViews
title: IUIAutomationMultipleViewPattern::GetCachedSupportedViews (uiautomationclient.h)
description: Retrieves a collection of control-specific view identifiers from the cache.helpviewer_keywords: ["GetCachedSupportedViews","GetCachedSupportedViews method [Windows Accessibility]","GetCachedSupportedViews method [Windows Accessibility]","IUIAutomationMultipleViewPattern interface","IUIAutomationMultipleViewPattern interface [Windows Accessibility]","GetCachedSupportedViews method","IUIAutomationMultipleViewPattern.GetCachedSupportedViews","IUIAutomationMultipleViewPattern::GetCachedSupportedViews","uiauto.uiauto_IUIAutomationMultipleViewPattern_GetCachedSupportedViews","uiauto_IUIAutomationMultipleViewPattern_GetCachedSupportedViews","uiautomationclient/IUIAutomationMultipleViewPattern::GetCachedSupportedViews","winauto.uiauto_IUIAutomationMultipleViewPattern_GetCachedSupportedViews"]
old-location: winauto\uiauto_IUIAutomationMultipleViewPattern_GetCachedSupportedViews.htm
tech.root: WinAuto
ms.assetid: 7d6874c2-adf9-441a-931e-15b65b7a427c
ms.date: 12/05/2018
ms.keywords: GetCachedSupportedViews, GetCachedSupportedViews method [Windows Accessibility], GetCachedSupportedViews method [Windows Accessibility],IUIAutomationMultipleViewPattern interface, IUIAutomationMultipleViewPattern interface [Windows Accessibility],GetCachedSupportedViews method, IUIAutomationMultipleViewPattern.GetCachedSupportedViews, IUIAutomationMultipleViewPattern::GetCachedSupportedViews, uiauto.uiauto_IUIAutomationMultipleViewPattern_GetCachedSupportedViews, uiauto_IUIAutomationMultipleViewPattern_GetCachedSupportedViews, uiautomationclient/IUIAutomationMultipleViewPattern::GetCachedSupportedViews, winauto.uiauto_IUIAutomationMultipleViewPattern_GetCachedSupportedViews
f1_keywords:
- uiautomationclient/IUIAutomationMultipleViewPattern.GetCachedSupportedViews
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
- IUIAutomationMultipleViewPattern.GetCachedSupportedViews
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomationMultipleViewPattern::GetCachedSupportedViews


## -description


Retrieves a collection of control-specific view identifiers from the cache.


## -parameters




### -param retVal [out, retval]

Type: <b><a href="https://docs.microsoft.com/windows/win32/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a>**</b>

Receives a pointer to an array of view identifiers.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-workingwithsafearrays">Best Practices for Using Safe Arrays</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationmultipleviewpattern">IUIAutomationMultipleViewPattern</a>
 

 

