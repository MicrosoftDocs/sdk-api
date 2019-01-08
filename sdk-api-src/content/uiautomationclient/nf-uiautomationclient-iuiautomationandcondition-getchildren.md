---
UID: NF:uiautomationclient.IUIAutomationAndCondition.GetChildren
title: IUIAutomationAndCondition::GetChildren
author: windows-sdk-content
description: Retrieves the conditions that make up this &#0034;and&#0034; condition.
old-location: winauto\uiauto_IUIAutomationAndCondition_GetChildren.htm
tech.root: WinAuto
ms.assetid: 6868fae6-74fb-4133-8dc5-73ce5f8a6f7b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetChildren, GetChildren method [Windows Accessibility], GetChildren method [Windows Accessibility],IUIAutomationAndCondition interface, IUIAutomationAndCondition interface [Windows Accessibility],GetChildren method, IUIAutomationAndCondition.GetChildren, IUIAutomationAndCondition::GetChildren, uiauto.uiauto_IUIAutomationAndCondition_GetChildren, uiauto_IUIAutomationAndCondition_GetChildren, uiautomationclient/IUIAutomationAndCondition::GetChildren, winauto.uiauto_IUIAutomationAndCondition_GetChildren
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
 - IUIAutomationAndCondition.GetChildren
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationAndCondition::GetChildren


## -description


Retrieves the conditions that make up this "and" condition.


## -parameters




### -param childArray [out, retval]

Type: <b><a href="https://docs.microsoft.com/dotnet/api/microsoft.visualstudio.ole.interop.safearray">SAFEARRAY</a>**</b>

Receives a pointer to the child conditions.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/07e87cfd-d565-41b5-a68d-b99dd191fa95">Best Practices for Using Safe Arrays</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/2543dd60-88cb-4477-9008-4ec8f9d8f287">GetChildrenAsNativeArray</a>



<a href="https://msdn.microsoft.com/f9808c48-dc98-465b-958d-223a8b7cc371">IUIAutomationAndCondition</a>



<b>Reference</b>
 

 

