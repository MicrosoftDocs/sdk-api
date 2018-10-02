---
UID: NF:uiautomationclient.IUIAutomationNotCondition.GetChild
title: IUIAutomationNotCondition::GetChild
author: windows-sdk-content
description: Retrieves the condition of which this condition is the negative.
old-location: winauto\uiauto_IUIAutomationNotCondition_GetChild.htm
tech.root: WinAuto
ms.assetid: 5d3a5df4-045a-41bf-aa98-3e9ac20c1c52
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetChild, GetChild method [Windows Accessibility], GetChild method [Windows Accessibility],IUIAutomationNotCondition interface, IUIAutomationNotCondition interface [Windows Accessibility],GetChild method, IUIAutomationNotCondition.GetChild, IUIAutomationNotCondition::GetChild, uiauto.uiauto_IUIAutomationNotCondition_GetChild, uiauto_IUIAutomationNotCondition_GetChild, uiautomationclient/IUIAutomationNotCondition::GetChild, winauto.uiauto_IUIAutomationNotCondition_GetChild
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
 - IUIAutomationNotCondition.GetChild
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationNotCondition::GetChild


## -description


Retrieves the condition of which this condition is the negative.


## -parameters




### -param condition [out, retval]

Type: <b><a href="https://msdn.microsoft.com/66515d42-2b98-4923-b326-9fec557345b7">IUIAutomationCondition</a>**</b>

Receives a pointer to the condition.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The returned condition is the one that was used in creating this condition.
			




## -see-also




<a href="https://msdn.microsoft.com/183603f9-6e5b-4c44-b6b2-c363b4d150c3">CreateNotCondition</a>



<a href="https://msdn.microsoft.com/63745e87-1571-47cb-b4d2-6909d834e97b">IUIAutomationNotCondition</a>
 

 

