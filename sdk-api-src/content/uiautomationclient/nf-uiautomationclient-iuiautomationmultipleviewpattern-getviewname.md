---
UID: NF:uiautomationclient.IUIAutomationMultipleViewPattern.GetViewName
title: IUIAutomationMultipleViewPattern::GetViewName (uiautomationclient.h)
description: Retrieves the name of a control-specific view. (IUIAutomationMultipleViewPattern.GetViewName)
helpviewer_keywords: ["GetViewName","GetViewName method [Windows Accessibility]","GetViewName method [Windows Accessibility]","IUIAutomationMultipleViewPattern interface","IUIAutomationMultipleViewPattern interface [Windows Accessibility]","GetViewName method","IUIAutomationMultipleViewPattern.GetViewName","IUIAutomationMultipleViewPattern::GetViewName","uiauto.uiauto_IUIAutomationMultipleViewPattern_GetViewName","uiauto_IUIAutomationMultipleViewPattern_GetViewName","uiautomationclient/IUIAutomationMultipleViewPattern::GetViewName","winauto.uiauto_IUIAutomationMultipleViewPattern_GetViewName"]
old-location: winauto\uiauto_IUIAutomationMultipleViewPattern_GetViewName.htm
tech.root: WinAuto
ms.assetid: cad994dc-ee7c-41a3-a878-75a79225b5f8
ms.date: 12/05/2018
ms.keywords: GetViewName, GetViewName method [Windows Accessibility], GetViewName method [Windows Accessibility],IUIAutomationMultipleViewPattern interface, IUIAutomationMultipleViewPattern interface [Windows Accessibility],GetViewName method, IUIAutomationMultipleViewPattern.GetViewName, IUIAutomationMultipleViewPattern::GetViewName, uiauto.uiauto_IUIAutomationMultipleViewPattern_GetViewName, uiauto_IUIAutomationMultipleViewPattern_GetViewName, uiautomationclient/IUIAutomationMultipleViewPattern::GetViewName, winauto.uiauto_IUIAutomationMultipleViewPattern_GetViewName
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
 - IUIAutomationMultipleViewPattern::GetViewName
 - uiautomationclient/IUIAutomationMultipleViewPattern::GetViewName
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
 - IUIAutomationMultipleViewPattern.GetViewName
---

# IUIAutomationMultipleViewPattern::GetViewName


## -description

Retrieves the name of a control-specific view.

## -parameters

### -param view [in]

Type: <b>int</b>

The identifier of the view.

### -param name [out, retval]

Type: <b>BSTR*</b>

Receives a pointer to a localized view name.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.
