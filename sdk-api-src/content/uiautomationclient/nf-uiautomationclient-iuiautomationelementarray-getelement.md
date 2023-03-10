---
UID: NF:uiautomationclient.IUIAutomationElementArray.GetElement
title: IUIAutomationElementArray::GetElement (uiautomationclient.h)
description: Retrieves a Microsoft UI Automation element from the collection.
helpviewer_keywords: ["GetElement","GetElement method [Windows Accessibility]","GetElement method [Windows Accessibility]","IUIAutomationElementArray interface","IUIAutomationElementArray interface [Windows Accessibility]","GetElement method","IUIAutomationElementArray.GetElement","IUIAutomationElementArray::GetElement","uiauto.uiauto_IUIAutomationElementArray_GetElement","uiauto_IUIAutomationElementArray_GetElement","uiautomationclient/IUIAutomationElementArray::GetElement","winauto.uiauto_IUIAutomationElementArray_GetElement"]
old-location: winauto\uiauto_IUIAutomationElementArray_GetElement.htm
tech.root: WinAuto
ms.assetid: c8651061-3a17-49d0-abc6-78ce3fa02363
ms.date: 12/05/2018
ms.keywords: GetElement, GetElement method [Windows Accessibility], GetElement method [Windows Accessibility],IUIAutomationElementArray interface, IUIAutomationElementArray interface [Windows Accessibility],GetElement method, IUIAutomationElementArray.GetElement, IUIAutomationElementArray::GetElement, uiauto.uiauto_IUIAutomationElementArray_GetElement, uiauto_IUIAutomationElementArray_GetElement, uiautomationclient/IUIAutomationElementArray::GetElement, winauto.uiauto_IUIAutomationElementArray_GetElement
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
 - IUIAutomationElementArray::GetElement
 - uiautomationclient/IUIAutomationElementArray::GetElement
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
 - IUIAutomationElementArray.GetElement
---

# IUIAutomationElementArray::GetElement


## -description

Retrieves a Microsoft UI Automation element from the collection.

## -parameters

### -param index [in]

Type: <b>int</b>

The zero-based index of the element.

### -param element [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>**</b>

Receives a pointer to the element.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelementarray">IUIAutomationElementArray</a>