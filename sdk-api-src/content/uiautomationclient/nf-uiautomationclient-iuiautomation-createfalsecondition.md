---
UID: NF:uiautomationclient.IUIAutomation.CreateFalseCondition
title: IUIAutomation::CreateFalseCondition
author: windows-sdk-content
description: Creates a condition that is always false.
old-location: winauto\uiauto_IUIAutomation_CreateFalseCondition.htm
tech.root: WinAuto
ms.assetid: 8fee46b7-a186-48b8-8fc0-f9844a2b6d8d
ms.author: windowssdkdev
ms.date: 10/23/2018
ms.keywords: CreateFalseCondition, CreateFalseCondition method [Windows Accessibility], CreateFalseCondition method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],CreateFalseCondition method, IUIAutomation.CreateFalseCondition, IUIAutomation::CreateFalseCondition, uiauto.uiauto_IUIAutomation_CreateFalseCondition, uiauto_IUIAutomation_CreateFalseCondition, uiautomationclient/IUIAutomation::CreateFalseCondition, winauto.uiauto_IUIAutomation_CreateFalseCondition
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
 - IUIAutomation.CreateFalseCondition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomation::CreateFalseCondition


## -description


Creates a condition that is always false.


## -parameters




### -param newCondition [out, retval]

Type: <b><a href="https://msdn.microsoft.com/66515d42-2b98-4923-b326-9fec557345b7">IUIAutomationCondition</a>**</b>

Receives a pointer to the false condition.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method exists only for symmetry with <a href="https://msdn.microsoft.com/02f55293-5d2d-4578-9c31-3ed04dac428e">IUIAutomation::CreateTrueCondition</a>. A false condition will never enable a match with UI Automation elements, and it cannot usefully be combined with any other condition.




## -see-also




<a href="https://msdn.microsoft.com/ead73c6d-7fb8-4e00-b027-5d747268af08">FindAll</a>



<a href="https://msdn.microsoft.com/acf16f88-2b68-4fd4-b715-b3a61340bdd0">FindAllBuildCache</a>



<a href="https://msdn.microsoft.com/84098431-46e8-49bd-a258-337ad1d68f91">FindFirst</a>



<a href="https://msdn.microsoft.com/ecb10fbf-ff1d-4bd0-b036-1050560d82fe">FindFirstBuildCache</a>



<a href="https://msdn.microsoft.com/46b31ab6-39aa-4df8-a421-6369c32a9605">IUIAutomation</a>



<a href="https://msdn.microsoft.com/66515d42-2b98-4923-b326-9fec557345b7">IUIAutomationCondition</a>



<b>Reference</b>
 

 

