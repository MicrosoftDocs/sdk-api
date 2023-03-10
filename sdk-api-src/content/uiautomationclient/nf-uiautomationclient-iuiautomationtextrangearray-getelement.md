---
UID: NF:uiautomationclient.IUIAutomationTextRangeArray.GetElement
title: IUIAutomationTextRangeArray::GetElement (uiautomationclient.h)
description: Retrieves a text range from the collection.
helpviewer_keywords: ["GetElement","GetElement method [Windows Accessibility]","GetElement method [Windows Accessibility]","IUIAutomationTextRangeArray interface","IUIAutomationTextRangeArray interface [Windows Accessibility]","GetElement method","IUIAutomationTextRangeArray.GetElement","IUIAutomationTextRangeArray::GetElement","uiauto.uiauto_IUIAutomationTextRangeArray_GetElement","uiauto_IUIAutomationTextRangeArray_GetElement","uiautomationclient/IUIAutomationTextRangeArray::GetElement","winauto.uiauto_IUIAutomationTextRangeArray_GetElement"]
old-location: winauto\uiauto_IUIAutomationTextRangeArray_GetElement.htm
tech.root: WinAuto
ms.assetid: b5077152-b06a-4391-a0c2-013362014b2b
ms.date: 12/05/2018
ms.keywords: GetElement, GetElement method [Windows Accessibility], GetElement method [Windows Accessibility],IUIAutomationTextRangeArray interface, IUIAutomationTextRangeArray interface [Windows Accessibility],GetElement method, IUIAutomationTextRangeArray.GetElement, IUIAutomationTextRangeArray::GetElement, uiauto.uiauto_IUIAutomationTextRangeArray_GetElement, uiauto_IUIAutomationTextRangeArray_GetElement, uiautomationclient/IUIAutomationTextRangeArray::GetElement, winauto.uiauto_IUIAutomationTextRangeArray_GetElement
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
 - IUIAutomationTextRangeArray::GetElement
 - uiautomationclient/IUIAutomationTextRangeArray::GetElement
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
 - IUIAutomationTextRangeArray.GetElement
---

# IUIAutomationTextRangeArray::GetElement


## -description

Retrieves a text range from the collection.

## -parameters

### -param index [in]

Type: <b>int</b>

The zero-based index of the item.

### -param element [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextrange">IUIAutomationTextRange</a>**</b>

Receives a pointer to the text range.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextrangearray">IUIAutomationTextRangeArray</a>



<a href="/windows/desktop/WinAuto/uiauto-ui-automation-textpattern-overview">UI Automation Support for Textual Content</a>