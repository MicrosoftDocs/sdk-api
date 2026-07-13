---
UID: NF:uiautomationclient.IUIAutomationTextRange.Compare
title: IUIAutomationTextRange::Compare (uiautomationclient.h)
description: Retrieves a value that specifies whether this text range has the same endpoints as another text range. (IUIAutomationTextRange.Compare)
helpviewer_keywords: ["Compare","Compare method [Windows Accessibility]","Compare method [Windows Accessibility]","IUIAutomationTextRange interface","IUIAutomationTextRange interface [Windows Accessibility]","Compare method","IUIAutomationTextRange.Compare","IUIAutomationTextRange::Compare","uiauto.uiauto_IUIAutomationTextRange_Compare","uiauto_IUIAutomationTextRange_Compare","uiautomationclient/IUIAutomationTextRange::Compare","winauto.uiauto_IUIAutomationTextRange_Compare"]
old-location: winauto\uiauto_IUIAutomationTextRange_Compare.htm
tech.root: WinAuto
ms.assetid: 4ccf78af-19b0-4bc9-a519-92df8276804e
ms.date: 12/05/2018
ms.keywords: Compare, Compare method [Windows Accessibility], Compare method [Windows Accessibility],IUIAutomationTextRange interface, IUIAutomationTextRange interface [Windows Accessibility],Compare method, IUIAutomationTextRange.Compare, IUIAutomationTextRange::Compare, uiauto.uiauto_IUIAutomationTextRange_Compare, uiauto_IUIAutomationTextRange_Compare, uiautomationclient/IUIAutomationTextRange::Compare, winauto.uiauto_IUIAutomationTextRange_Compare
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
 - IUIAutomationTextRange::Compare
 - uiautomationclient/IUIAutomationTextRange::Compare
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
 - IUIAutomationTextRange.Compare
---

# IUIAutomationTextRange::Compare


## -description

Retrieves a value that specifies whether this text range has the same endpoints as another text range.

## -parameters

### -param range [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextrange">IUIAutomationTextRange</a>*</b>

A pointer to  the text range to compare with this one.

### -param areSame [out, retval]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a>*</b>

Receives <b>TRUE</b> if the text ranges have the same endpoints, or <b>FALSE</b> if they do not.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method compares the endpoints of the two text ranges, not the text in the ranges. The ranges are identical if they share the same endpoints. If two text ranges have different endpoints, they are not identical even if the text in both ranges is exactly the same.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextrange">IUIAutomationTextRange</a>



<a href="/windows/desktop/WinAuto/uiauto-ui-automation-textpattern-overview">UI Automation Support for Textual Content</a>
