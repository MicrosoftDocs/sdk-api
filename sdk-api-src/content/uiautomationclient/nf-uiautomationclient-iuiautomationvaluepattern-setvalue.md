---
UID: NF:uiautomationclient.IUIAutomationValuePattern.SetValue
title: IUIAutomationValuePattern::SetValue (uiautomationclient.h)
description: Sets the value of the element.
helpviewer_keywords: ["IUIAutomationValuePattern interface [Windows Accessibility]","SetValue method","IUIAutomationValuePattern.SetValue","IUIAutomationValuePattern::SetValue","SetValue","SetValue method [Windows Accessibility]","SetValue method [Windows Accessibility]","IUIAutomationValuePattern interface","uiauto.uiauto_IUIAutomationValuePattern_SetValue","uiauto_IUIAutomationValuePattern_SetValue","uiautomationclient/IUIAutomationValuePattern::SetValue","winauto.uiauto_IUIAutomationValuePattern_SetValue"]
old-location: winauto\uiauto_IUIAutomationValuePattern_SetValue.htm
tech.root: WinAuto
ms.assetid: 9b4caa59-bda4-4cc6-b2d8-ff47ea292746
ms.date: 12/05/2018
ms.keywords: IUIAutomationValuePattern interface [Windows Accessibility],SetValue method, IUIAutomationValuePattern.SetValue, IUIAutomationValuePattern::SetValue, SetValue, SetValue method [Windows Accessibility], SetValue method [Windows Accessibility],IUIAutomationValuePattern interface, uiauto.uiauto_IUIAutomationValuePattern_SetValue, uiauto_IUIAutomationValuePattern_SetValue, uiautomationclient/IUIAutomationValuePattern::SetValue, winauto.uiauto_IUIAutomationValuePattern_SetValue
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
 - IUIAutomationValuePattern::SetValue
 - uiautomationclient/IUIAutomationValuePattern::SetValue
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
 - IUIAutomationValuePattern.SetValue
---

# IUIAutomationValuePattern::SetValue


## -description

Sets the value of the element.

## -parameters

### -param val [in]

Type: <b>BSTR</b>

The value to set.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_currentisenabled">CurrentIsEnabled</a> property must be <b>TRUE</b>, and the <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationvaluepattern-get_currentisreadonly">IUIAutomationValuePattern::CurrentIsReadOnly</a> property must be <b>FALSE</b>.