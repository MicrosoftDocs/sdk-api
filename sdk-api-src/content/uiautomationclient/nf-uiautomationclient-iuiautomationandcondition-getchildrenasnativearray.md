---
UID: NF:uiautomationclient.IUIAutomationAndCondition.GetChildrenAsNativeArray
title: IUIAutomationAndCondition::GetChildrenAsNativeArray
author: windows-sdk-content
description: Retrieves the conditions that make up this condition, as an ordinary array.
old-location: winauto\uiauto_IUIAutomationAndCondition_GetChildrenAsNativeArray.htm
tech.root: WinAuto
ms.assetid: 2543dd60-88cb-4477-9008-4ec8f9d8f287
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetChildrenAsNativeArray, GetChildrenAsNativeArray method [Windows Accessibility], GetChildrenAsNativeArray method [Windows Accessibility],IUIAutomationAndCondition interface, IUIAutomationAndCondition interface [Windows Accessibility],GetChildrenAsNativeArray method, IUIAutomationAndCondition.GetChildrenAsNativeArray, IUIAutomationAndCondition::GetChildrenAsNativeArray, uiauto.uiauto_IUIAutomationAndCondition_GetChildrenAsNativeArray, uiauto_IUIAutomationAndCondition_GetChildrenAsNativeArray, uiautomationclient/IUIAutomationAndCondition::GetChildrenAsNativeArray, winauto.uiauto_IUIAutomationAndCondition_GetChildrenAsNativeArray
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
 - IUIAutomationAndCondition.GetChildrenAsNativeArray
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationAndCondition::GetChildrenAsNativeArray


## -description


Retrieves the conditions that make up this condition, as an ordinary array.


## -parameters




### -param childArray [out]

Type: <b><a href="https://msdn.microsoft.com/66515d42-2b98-4923-b326-9fec557345b7">IUIAutomationCondition</a>***</b>

Receives a pointer to an  array of <a href="https://msdn.microsoft.com/66515d42-2b98-4923-b326-9fec557345b7">IUIAutomationCondition</a> interface pointers.


### -param childArrayCount [out]

Type: <b>int*</b>

Receives the number of elements in the array.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/f9808c48-dc98-465b-958d-223a8b7cc371">IUIAutomationAndCondition</a>



<a href="https://msdn.microsoft.com/6868fae6-74fb-4133-8dc5-73ce5f8a6f7b">IUIAutomationAndCondition::GetChildren</a>
 

 

