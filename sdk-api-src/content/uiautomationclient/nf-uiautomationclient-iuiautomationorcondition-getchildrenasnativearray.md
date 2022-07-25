---
UID: NF:uiautomationclient.IUIAutomationOrCondition.GetChildrenAsNativeArray
title: IUIAutomationOrCondition::GetChildrenAsNativeArray (uiautomationclient.h)
description: Retrieves the conditions that make up this &quot;or&quot; condition, as an ordinary array.
helpviewer_keywords: ["GetChildrenAsNativeArray","GetChildrenAsNativeArray method [Windows Accessibility]","GetChildrenAsNativeArray method [Windows Accessibility]","IUIAutomationOrCondition interface","IUIAutomationOrCondition interface [Windows Accessibility]","GetChildrenAsNativeArray method","IUIAutomationOrCondition.GetChildrenAsNativeArray","IUIAutomationOrCondition::GetChildrenAsNativeArray","uiauto.uiauto_IUIAutomationOrCondition_GetChildrenAsNativeArray","uiauto_IUIAutomationOrCondition_GetChildrenAsNativeArray","uiautomationclient/IUIAutomationOrCondition::GetChildrenAsNativeArray","winauto.uiauto_IUIAutomationOrCondition_GetChildrenAsNativeArray"]
old-location: winauto\uiauto_IUIAutomationOrCondition_GetChildrenAsNativeArray.htm
tech.root: WinAuto
ms.assetid: d8c45ccb-5e3c-4816-8ffe-6865a7794e8b
ms.date: 12/05/2018
ms.keywords: GetChildrenAsNativeArray, GetChildrenAsNativeArray method [Windows Accessibility], GetChildrenAsNativeArray method [Windows Accessibility],IUIAutomationOrCondition interface, IUIAutomationOrCondition interface [Windows Accessibility],GetChildrenAsNativeArray method, IUIAutomationOrCondition.GetChildrenAsNativeArray, IUIAutomationOrCondition::GetChildrenAsNativeArray, uiauto.uiauto_IUIAutomationOrCondition_GetChildrenAsNativeArray, uiauto_IUIAutomationOrCondition_GetChildrenAsNativeArray, uiautomationclient/IUIAutomationOrCondition::GetChildrenAsNativeArray, winauto.uiauto_IUIAutomationOrCondition_GetChildrenAsNativeArray
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
 - IUIAutomationOrCondition::GetChildrenAsNativeArray
 - uiautomationclient/IUIAutomationOrCondition::GetChildrenAsNativeArray
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
 - IUIAutomationOrCondition.GetChildrenAsNativeArray
---

# IUIAutomationOrCondition::GetChildrenAsNativeArray


## -description

Retrieves the conditions that make up this "or" condition, as an ordinary array.

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

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationorcondition">IUIAutomationOrCondition</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationorcondition-getchildren">IUIAutomationOrCondition::GetChildren</a>