---
UID: NF:uiautomationclient.IUIAutomation.CompareRuntimeIds
title: IUIAutomation::CompareRuntimeIds (uiautomationclient.h)
description: Compares two integer arrays containing run-time identifiers (IDs) to determine whether their content is the same and they belong to the same UI element.
helpviewer_keywords: ["CompareRuntimeIds","CompareRuntimeIds method [Windows Accessibility]","CompareRuntimeIds method [Windows Accessibility]","IUIAutomation interface","IUIAutomation interface [Windows Accessibility]","CompareRuntimeIds method","IUIAutomation.CompareRuntimeIds","IUIAutomation::CompareRuntimeIds","uiauto.uiauto_IUIAutomation_CompareRuntimeIds","uiauto_IUIAutomation_CompareRuntimeIds","uiautomationclient/IUIAutomation::CompareRuntimeIds","winauto.uiauto_IUIAutomation_CompareRuntimeIds"]
old-location: winauto\uiauto_IUIAutomation_CompareRuntimeIds.htm
tech.root: WinAuto
ms.assetid: b0c481eb-3545-439c-bf6a-347b98ea35de
ms.date: 12/05/2018
ms.keywords: CompareRuntimeIds, CompareRuntimeIds method [Windows Accessibility], CompareRuntimeIds method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],CompareRuntimeIds method, IUIAutomation.CompareRuntimeIds, IUIAutomation::CompareRuntimeIds, uiauto.uiauto_IUIAutomation_CompareRuntimeIds, uiauto_IUIAutomation_CompareRuntimeIds, uiautomationclient/IUIAutomation::CompareRuntimeIds, winauto.uiauto_IUIAutomation_CompareRuntimeIds
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
 - IUIAutomation::CompareRuntimeIds
 - uiautomationclient/IUIAutomation::CompareRuntimeIds
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
 - IUIAutomation.CompareRuntimeIds
---

# IUIAutomation::CompareRuntimeIds


## -description

Compares two integer arrays containing run-time identifiers (IDs) to determine whether their content is the same and they belong to the same UI element.

## -parameters

### -param runtimeId1 [in]

Type: <b><a href="/windows/win32/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a>*</b>

The first ID to compare.

### -param runtimeId2 [in]

Type: <b><a href="/windows/win32/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a>*</b>

The second ID to compare

### -param areSame [out, retval]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a>*</b>

Receives <b>TRUE</b> if the IDs are the same, or <b>FALSE</b> otherwise.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-workingwithsafearrays">Best Practices for Using Safe Arrays</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-compareelements">CompareElements</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-getruntimeid">GetRuntimeId</a>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation">IUIAutomation</a>



<b>Reference</b>