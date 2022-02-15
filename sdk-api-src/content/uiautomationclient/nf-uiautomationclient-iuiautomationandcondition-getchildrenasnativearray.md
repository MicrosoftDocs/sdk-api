---
UID: NF:uiautomationclient.IUIAutomationAndCondition.GetChildrenAsNativeArray
title: IUIAutomationAndCondition::GetChildrenAsNativeArray (uiautomationclient.h)
description: Retrieves the conditions that make up this &quot;and&quot; condition, as an ordinary array.
helpviewer_keywords: ["GetChildrenAsNativeArray","GetChildrenAsNativeArray method [Windows Accessibility]","GetChildrenAsNativeArray method [Windows Accessibility]","IUIAutomationAndCondition interface","IUIAutomationAndCondition interface [Windows Accessibility]","GetChildrenAsNativeArray method","IUIAutomationAndCondition.GetChildrenAsNativeArray","IUIAutomationAndCondition::GetChildrenAsNativeArray","uiauto.uiauto_IUIAutomationAndCondition_GetChildrenAsNativeArray","uiauto_IUIAutomationAndCondition_GetChildrenAsNativeArray","uiautomationclient/IUIAutomationAndCondition::GetChildrenAsNativeArray","winauto.uiauto_IUIAutomationAndCondition_GetChildrenAsNativeArray"]
old-location: winauto\uiauto_IUIAutomationAndCondition_GetChildrenAsNativeArray.htm
tech.root: WinAuto
ms.assetid: 2543dd60-88cb-4477-9008-4ec8f9d8f287
ms.date: 12/05/2018
ms.keywords: GetChildrenAsNativeArray, GetChildrenAsNativeArray method [Windows Accessibility], GetChildrenAsNativeArray method [Windows Accessibility],IUIAutomationAndCondition interface, IUIAutomationAndCondition interface [Windows Accessibility],GetChildrenAsNativeArray method, IUIAutomationAndCondition.GetChildrenAsNativeArray, IUIAutomationAndCondition::GetChildrenAsNativeArray, uiauto.uiauto_IUIAutomationAndCondition_GetChildrenAsNativeArray, uiauto_IUIAutomationAndCondition_GetChildrenAsNativeArray, uiautomationclient/IUIAutomationAndCondition::GetChildrenAsNativeArray, winauto.uiauto_IUIAutomationAndCondition_GetChildrenAsNativeArray
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
 - IUIAutomationAndCondition::GetChildrenAsNativeArray
 - uiautomationclient/IUIAutomationAndCondition::GetChildrenAsNativeArray
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
 - IUIAutomationAndCondition.GetChildrenAsNativeArray
---

# IUIAutomationAndCondition::GetChildrenAsNativeArray


## -description

Retrieves the conditions that make up this "and" condition, as an ordinary array.

## -parameters

### -param childArray [out]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition">IUIAutomationCondition</a>***</b>

Receives a pointer to an  array of <a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition">IUIAutomationCondition</a> interface pointers.

### -param childArrayCount [out]

Type: <b>int*</b>

Receives the number of elements in the array.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationandcondition">IUIAutomationAndCondition</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationandcondition-getchildren">IUIAutomationAndCondition::GetChildren</a>