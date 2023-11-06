---
UID: NF:uiautomationclient.IUIAutomationTextRange.CompareEndpoints
title: IUIAutomationTextRange::CompareEndpoints (uiautomationclient.h)
description: Retrieves a value that specifies whether the start or end endpoint of this text range is the same as the start or end endpoint of another text range.
helpviewer_keywords: ["CompareEndpoints","CompareEndpoints method [Windows Accessibility]","CompareEndpoints method [Windows Accessibility]","IUIAutomationTextRange interface","IUIAutomationTextRange interface [Windows Accessibility]","CompareEndpoints method","IUIAutomationTextRange.CompareEndpoints","IUIAutomationTextRange::CompareEndpoints","uiauto.uiauto_IUIAutomationTextRange_CompareEndpoints","uiauto_IUIAutomationTextRange_CompareEndpoints","uiautomationclient/IUIAutomationTextRange::CompareEndpoints","winauto.uiauto_IUIAutomationTextRange_CompareEndpoints"]
old-location: winauto\uiauto_IUIAutomationTextRange_CompareEndpoints.htm
tech.root: WinAuto
ms.assetid: 7071ae46-3f2d-4fdb-9908-366ac1fde691
ms.date: 12/05/2018
ms.keywords: CompareEndpoints, CompareEndpoints method [Windows Accessibility], CompareEndpoints method [Windows Accessibility],IUIAutomationTextRange interface, IUIAutomationTextRange interface [Windows Accessibility],CompareEndpoints method, IUIAutomationTextRange.CompareEndpoints, IUIAutomationTextRange::CompareEndpoints, uiauto.uiauto_IUIAutomationTextRange_CompareEndpoints, uiauto_IUIAutomationTextRange_CompareEndpoints, uiautomationclient/IUIAutomationTextRange::CompareEndpoints, winauto.uiauto_IUIAutomationTextRange_CompareEndpoints
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
 - IUIAutomationTextRange::CompareEndpoints
 - uiautomationclient/IUIAutomationTextRange::CompareEndpoints
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
 - IUIAutomationTextRange.CompareEndpoints
---

# IUIAutomationTextRange::CompareEndpoints


## -description

Retrieves a value that specifies whether the start or end endpoint of this text range is the same as the start or end endpoint of another text range.

## -parameters

### -param srcEndPoint [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint">TextPatternRangeEndpoint</a></b>

A value indicating whether the start or end endpoint of this text range is to be compared.

### -param range [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextrange">IUIAutomationTextRange</a>*</b>

A pointer to the text range to compare.

### -param targetEndPoint [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint">TextPatternRangeEndpoint</a></b>

A value indicating whether the start or end endpoint of <i>range</i> is to be compared.

### -param compValue [out, retval]

Type: <b>int*</b>

Receives a negative value if the caller's endpoint occurs earlier in the text than the target endpoint; 0 if the caller's endpoint is at the same location as the target endpoint; or a positive value if the caller's endpoint occurs later in the text than the target endpoint.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextrange">IUIAutomationTextRange</a>



<a href="/windows/desktop/WinAuto/uiauto-ui-automation-textpattern-overview">UI Automation Support for Textual Content</a>