---
UID: NF:uiautomationclient.IUIAutomationAndCondition.GetChildren
title: IUIAutomationAndCondition::GetChildren (uiautomationclient.h)
description: Retrieves the conditions that make up this &quot;and&quot; condition.
helpviewer_keywords: ["GetChildren","GetChildren method [Windows Accessibility]","GetChildren method [Windows Accessibility]","IUIAutomationAndCondition interface","IUIAutomationAndCondition interface [Windows Accessibility]","GetChildren method","IUIAutomationAndCondition.GetChildren","IUIAutomationAndCondition::GetChildren","uiauto.uiauto_IUIAutomationAndCondition_GetChildren","uiauto_IUIAutomationAndCondition_GetChildren","uiautomationclient/IUIAutomationAndCondition::GetChildren","winauto.uiauto_IUIAutomationAndCondition_GetChildren"]
old-location: winauto\uiauto_IUIAutomationAndCondition_GetChildren.htm
tech.root: WinAuto
ms.assetid: 6868fae6-74fb-4133-8dc5-73ce5f8a6f7b
ms.date: 12/05/2018
ms.keywords: GetChildren, GetChildren method [Windows Accessibility], GetChildren method [Windows Accessibility],IUIAutomationAndCondition interface, IUIAutomationAndCondition interface [Windows Accessibility],GetChildren method, IUIAutomationAndCondition.GetChildren, IUIAutomationAndCondition::GetChildren, uiauto.uiauto_IUIAutomationAndCondition_GetChildren, uiauto_IUIAutomationAndCondition_GetChildren, uiautomationclient/IUIAutomationAndCondition::GetChildren, winauto.uiauto_IUIAutomationAndCondition_GetChildren
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
 - IUIAutomationAndCondition::GetChildren
 - uiautomationclient/IUIAutomationAndCondition::GetChildren
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
 - IUIAutomationAndCondition.GetChildren
---

# IUIAutomationAndCondition::GetChildren


## -description

Retrieves the conditions that make up this "and" condition.

## -parameters

### -param childArray [out, retval]

Type: <b><a href="/dotnet/api/microsoft.visualstudio.ole.interop.safearray">SAFEARRAY</a>**</b>

Receives a pointer to the child conditions.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-workingwithsafearrays">Best Practices for Using Safe Arrays</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationandcondition-getchildrenasnativearray">GetChildrenAsNativeArray</a>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationandcondition">IUIAutomationAndCondition</a>



<b>Reference</b>