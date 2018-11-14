---
UID: NF:uiautomationclient.IUIAutomation.CreateTrueCondition
title: IUIAutomation::CreateTrueCondition
author: windows-sdk-content
description: Retrieves a predefined condition that selects all elements.
old-location: winauto\uiauto_IUIAutomation_CreateTrueCondition.htm
tech.root: WinAuto
ms.assetid: 02f55293-5d2d-4578-9c31-3ed04dac428e
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: CreateTrueCondition, CreateTrueCondition method [Windows Accessibility], CreateTrueCondition method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],CreateTrueCondition method, IUIAutomation.CreateTrueCondition, IUIAutomation::CreateTrueCondition, uiauto.uiauto_IUIAutomation_CreateTrueCondition, uiauto_IUIAutomation_CreateTrueCondition, uiautomationclient/IUIAutomation::CreateTrueCondition, winauto.uiauto_IUIAutomation_CreateTrueCondition
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
 - IUIAutomation.CreateTrueCondition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- uiautomationclient.h
: 
- IUIAutomation.CreateTrueCondition
: 
---

# IUIAutomation::CreateTrueCondition


## -description


Retrieves a predefined condition that selects all elements.


## -parameters




### -param newCondition [out, retval]

Type: <b><a href="https://msdn.microsoft.com/66515d42-2b98-4923-b326-9fec557345b7">IUIAutomationCondition</a>**</b>

Receives a pointer to the true condition.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/8fee46b7-a186-48b8-8fc0-f9844a2b6d8d">CreateFalseCondition</a>



<a href="https://msdn.microsoft.com/46b31ab6-39aa-4df8-a421-6369c32a9605">IUIAutomation</a>



<a href="https://msdn.microsoft.com/66515d42-2b98-4923-b326-9fec557345b7">IUIAutomationCondition</a>
 

 

