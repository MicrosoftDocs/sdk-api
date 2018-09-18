---
UID: NF:uiautomationclient.IUIAutomationOrCondition.GetChildren
title: IUIAutomationOrCondition::GetChildren
author: windows-sdk-content
description: Retrieves the conditions that make up this condition.
old-location: winauto\uiauto_IUIAutomationOrCondition_GetChildren.htm
tech.root: WinAuto
ms.assetid: b1af107d-2916-4061-9515-002c3af6eb00
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: GetChildren, GetChildren method [Windows Accessibility], GetChildren method [Windows Accessibility],IUIAutomationOrCondition interface, IUIAutomationOrCondition interface [Windows Accessibility],GetChildren method, IUIAutomationOrCondition.GetChildren, IUIAutomationOrCondition::GetChildren, uiauto.uiauto_IUIAutomationOrCondition_GetChildren, uiauto_IUIAutomationOrCondition_GetChildren, uiautomationclient/IUIAutomationOrCondition::GetChildren, winauto.uiauto_IUIAutomationOrCondition_GetChildren
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
---

# IUIAutomationOrCondition::GetChildren


## -description


Retrieves the conditions that make up this condition.


## -parameters




### -param childArray [out, retval]

Type: <b><a href="http://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a>**</b>

Receives a pointer to the child conditions.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/07e87cfd-d565-41b5-a68d-b99dd191fa95">Best Practices for Using Safe Arrays</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/d8c45ccb-5e3c-4816-8ffe-6865a7794e8b">GetChildrenAsNativeArray</a>



<a href="https://msdn.microsoft.com/323dedd5-2799-4fcc-bc8c-56b39ab7f882">IUIAutomationOrCondition</a>



<b>Reference</b>
 

 

