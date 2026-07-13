---
UID: NF:uiautomationclient.IUIAutomation.CompareElements
title: IUIAutomation::CompareElements (uiautomationclient.h)
description: Compares two UI Automation elements to determine whether they represent the same underlying UI element.
helpviewer_keywords: ["CompareElements","CompareElements method [Windows Accessibility]","CompareElements method [Windows Accessibility]","IUIAutomation interface","IUIAutomation interface [Windows Accessibility]","CompareElements method","IUIAutomation.CompareElements","IUIAutomation::CompareElements","uiauto.uiauto_IUIAutomation_CompareElements","uiauto_IUIAutomation_CompareElements","uiautomationclient/IUIAutomation::CompareElements","winauto.uiauto_IUIAutomation_CompareElements"]
old-location: winauto\uiauto_IUIAutomation_CompareElements.htm
tech.root: WinAuto
ms.assetid: e4daa3c3-24fb-41df-a1b1-bd6545a47e51
ms.date: 12/05/2018
ms.keywords: CompareElements, CompareElements method [Windows Accessibility], CompareElements method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],CompareElements method, IUIAutomation.CompareElements, IUIAutomation::CompareElements, uiauto.uiauto_IUIAutomation_CompareElements, uiauto_IUIAutomation_CompareElements, uiautomationclient/IUIAutomation::CompareElements, winauto.uiauto_IUIAutomation_CompareElements
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
 - IUIAutomation::CompareElements
 - uiautomationclient/IUIAutomation::CompareElements
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
 - IUIAutomation.CompareElements
---

# IUIAutomation::CompareElements


## -description

Compares two UI Automation elements to determine whether they represent the same underlying UI element.

## -parameters

### -param el1 [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>*</b>

A pointer to the first element to compare.

### -param el2 [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>*</b>

A pointer to the second element to compare.

### -param areSame [out, retval]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a>*</b>

Receives <b>TRUE</b> if the run-time identifiers of the elements are the same, or <b>FALSE</b> otherwise.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation">IUIAutomation</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-compareruntimeids">IUIAutomation::CompareRuntimeIds</a>