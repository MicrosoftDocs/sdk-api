---
UID: NF:uiautomationclient.IUIAutomationOrCondition.GetChildrenAsNativeArray
title: IUIAutomationOrCondition::GetChildrenAsNativeArray
author: windows-sdk-content
description: Retrieves the conditions that make up this &#0034;or&#0034; condition, as an ordinary array.
old-location: winauto\uiauto_IUIAutomationOrCondition_GetChildrenAsNativeArray.htm
tech.root: WinAuto
ms.assetid: d8c45ccb-5e3c-4816-8ffe-6865a7794e8b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetChildrenAsNativeArray, GetChildrenAsNativeArray method [Windows Accessibility], GetChildrenAsNativeArray method [Windows Accessibility],IUIAutomationOrCondition interface, IUIAutomationOrCondition interface [Windows Accessibility],GetChildrenAsNativeArray method, IUIAutomationOrCondition.GetChildrenAsNativeArray, IUIAutomationOrCondition::GetChildrenAsNativeArray, uiauto.uiauto_IUIAutomationOrCondition_GetChildrenAsNativeArray, uiauto_IUIAutomationOrCondition_GetChildrenAsNativeArray, uiautomationclient/IUIAutomationOrCondition::GetChildrenAsNativeArray, winauto.uiauto_IUIAutomationOrCondition_GetChildrenAsNativeArray
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
 - IUIAutomationOrCondition.GetChildrenAsNativeArray
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationOrCondition::GetChildrenAsNativeArray


## -description


Retrieves the conditions that make up this "or" condition, as an ordinary array.


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




<a href="https://msdn.microsoft.com/323dedd5-2799-4fcc-bc8c-56b39ab7f882">IUIAutomationOrCondition</a>



<a href="https://msdn.microsoft.com/b1af107d-2916-4061-9515-002c3af6eb00">IUIAutomationOrCondition::GetChildren</a>
 

 

