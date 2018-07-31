---
UID: NF:uiautomationclient.IUIAutomation.CreateOrCondition
title: IUIAutomation::CreateOrCondition
author: windows-sdk-content
description: Creates a combination of two conditions where a match exists if either of the conditions is true.
old-location: winauto\uiauto_IUIAutomation_CreateOrCondition.htm
old-project: WinAuto
ms.assetid: 17e83b94-21f0-44b6-87be-3fc44b0dc5a0
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: CreateOrCondition, CreateOrCondition method [Windows Accessibility], CreateOrCondition method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],CreateOrCondition method, IUIAutomation.CreateOrCondition, IUIAutomation::CreateOrCondition, uiauto.uiauto_IUIAutomation_CreateOrCondition, uiauto_IUIAutomation_CreateOrCondition, uiautomationclient/IUIAutomation::CreateOrCondition, winauto.uiauto_IUIAutomation_CreateOrCondition
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: "*UI_ANIMATION_KEYFRAME"
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomation.CreateOrCondition
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomation::CreateOrCondition


## -description


Creates a combination of two conditions where a match exists if either of the conditions is true. 


## -parameters




### -param condition1 [in]

Type: <b><a href="https://msdn.microsoft.com/66515d42-2b98-4923-b326-9fec557345b7">IUIAutomationCondition</a>*</b>

A pointer to the first condition.


### -param condition2 [in]

Type: <b><a href="https://msdn.microsoft.com/66515d42-2b98-4923-b326-9fec557345b7">IUIAutomationCondition</a>*</b>

A pointer to the second condition.


### -param newCondition [out, retval]

Type: <b><a href="https://msdn.microsoft.com/66515d42-2b98-4923-b326-9fec557345b7">IUIAutomationCondition</a>**</b>

Receives a pointer to the combined condition.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <b>CreateOrCondition</b> method calls <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a> on the <i>condition1</i> and <i>condition2</i> pointers. This means you can call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> on those two pointers after the call to <b>CreateOrCondition</b> returns  without invalidating the pointer returned from <b>CreateOrCondition</b>. When you call <b>Release</b> on the pointer returned from  <b>CreateOrCondition</b>, UI Automation calls <b>Release</b> on the <i>condition1</i> and <i>condition2</i> pointers.




## -see-also




<a href="https://msdn.microsoft.com/acd15fd0-ac15-4477-8e89-4d7a4f9c93c6">CreateOrConditionFromArray</a>



<a href="https://msdn.microsoft.com/393c777c-f262-462b-ac59-035f590bee1c">CreateOrConditionFromNativeArray</a>



<a href="https://msdn.microsoft.com/ead73c6d-7fb8-4e00-b027-5d747268af08">FindAll</a>



<a href="https://msdn.microsoft.com/acf16f88-2b68-4fd4-b715-b3a61340bdd0">FindAllBuildCache</a>



<a href="https://msdn.microsoft.com/84098431-46e8-49bd-a258-337ad1d68f91">FindFirst</a>



<a href="https://msdn.microsoft.com/ecb10fbf-ff1d-4bd0-b036-1050560d82fe">FindFirstBuildCache</a>



<a href="https://msdn.microsoft.com/46b31ab6-39aa-4df8-a421-6369c32a9605">IUIAutomation</a>



<a href="https://msdn.microsoft.com/66515d42-2b98-4923-b326-9fec557345b7">IUIAutomationCondition</a>



<b>Reference</b>
 

 

