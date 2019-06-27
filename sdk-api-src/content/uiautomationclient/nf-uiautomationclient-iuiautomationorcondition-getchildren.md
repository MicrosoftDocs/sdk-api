---
UID: NF:uiautomationclient.IUIAutomationOrCondition.GetChildren
title: IUIAutomationOrCondition::GetChildren (uiautomationclient.h)
author: windows-sdk-content
description: Retrieves the conditions that make up this &#0034;or&#0034; condition.
old-location: winauto\uiauto_IUIAutomationOrCondition_GetChildren.htm
tech.root: WinAuto
ms.assetid: b1af107d-2916-4061-9515-002c3af6eb00
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetChildren, GetChildren method [Windows Accessibility], GetChildren method [Windows Accessibility],IUIAutomationOrCondition interface, IUIAutomationOrCondition interface [Windows Accessibility],GetChildren method, IUIAutomationOrCondition.GetChildren, IUIAutomationOrCondition::GetChildren, uiauto.uiauto_IUIAutomationOrCondition_GetChildren, uiauto_IUIAutomationOrCondition_GetChildren, uiautomationclient/IUIAutomationOrCondition::GetChildren, winauto.uiauto_IUIAutomationOrCondition_GetChildren
ms.topic: method
f1_keywords: 
 - "uiautomationclient/IUIAutomationOrCondition.GetChildren"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomationOrCondition.GetChildren
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomationOrCondition::GetChildren


## -description


Retrieves the conditions that make up this "or" condition.


## -parameters




### -param childArray [out, retval]

Type: <b><a href="https://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a>**</b>

Receives a pointer to the child conditions.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-workingwithsafearrays">Best Practices for Using Safe Arrays</a>



<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationorcondition-getchildrenasnativearray">GetChildrenAsNativeArray</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationorcondition">IUIAutomationOrCondition</a>



<b>Reference</b>
 

 

