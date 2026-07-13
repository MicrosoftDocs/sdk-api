---
UID: NF:uiautomationclient.IUIAutomationTextRange.Clone
title: IUIAutomationTextRange::Clone (uiautomationclient.h)
description: Retrieves a new IUIAutomationTextRange identical to the original and inheriting all properties of the original.
helpviewer_keywords: ["Clone","Clone method [Windows Accessibility]","Clone method [Windows Accessibility]","IUIAutomationTextRange interface","IUIAutomationTextRange interface [Windows Accessibility]","Clone method","IUIAutomationTextRange.Clone","IUIAutomationTextRange::Clone","uiauto.uiauto_IUIAutomationTextRange_Clone","uiauto_IUIAutomationTextRange_Clone","uiautomationclient/IUIAutomationTextRange::Clone","winauto.uiauto_IUIAutomationTextRange_Clone"]
old-location: winauto\uiauto_IUIAutomationTextRange_Clone.htm
tech.root: WinAuto
ms.assetid: 0f41fecf-fd66-443f-bc4d-23c05a4d3824
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Windows Accessibility], Clone method [Windows Accessibility],IUIAutomationTextRange interface, IUIAutomationTextRange interface [Windows Accessibility],Clone method, IUIAutomationTextRange.Clone, IUIAutomationTextRange::Clone, uiauto.uiauto_IUIAutomationTextRange_Clone, uiauto_IUIAutomationTextRange_Clone, uiautomationclient/IUIAutomationTextRange::Clone, winauto.uiauto_IUIAutomationTextRange_Clone
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
 - IUIAutomationTextRange::Clone
 - uiautomationclient/IUIAutomationTextRange::Clone
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
 - IUIAutomationTextRange.Clone
---

# IUIAutomationTextRange::Clone


## -description

Retrieves a new <a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextrange">IUIAutomationTextRange</a> identical to the original and inheriting all properties of the original.

## -parameters

### -param clonedRange [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextrange">IUIAutomationTextRange</a>**</b>

Receives a pointer to the new text range.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The new range can be manipulated independently of the original.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextrange">IUIAutomationTextRange</a>



<a href="/windows/desktop/WinAuto/uiauto-ui-automation-textpattern-overview">UI Automation Support for Textual Content</a>