---
UID: NF:uiautomationclient.IUIAutomation.CreateOrConditionFromArray
title: IUIAutomation::CreateOrConditionFromArray
author: windows-driver-content
description: Creates a combination of two or more conditions where a match exists if any of the conditions is true.
old-location: winauto\uiauto_IUIAutomation_CreateOrConditionFromArray.htm
old-project: WinAuto
ms.assetid: acd15fd0-ac15-4477-8e89-4d7a4f9c93c6
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: CreateOrConditionFromArray, CreateOrConditionFromArray method [Windows Accessibility], CreateOrConditionFromArray method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],CreateOrConditionFromArray method, IUIAutomation.CreateOrConditionFromArray, IUIAutomation::CreateOrConditionFromArray, uiauto.uiauto_IUIAutomation_CreateOrConditionFromArray, uiauto_IUIAutomation_CreateOrConditionFromArray, uiautomationclient/IUIAutomation::CreateOrConditionFromArray, winauto.uiauto_IUIAutomation_CreateOrConditionFromArray
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAutomationClient.h
api_name:
-	IUIAutomation.CreateOrConditionFromArray
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomation::CreateOrConditionFromArray


## -description


Creates a combination of two or more conditions where a match exists if any of the conditions is true. 


## -parameters




### -param conditions [in]

Type: <b><a href="http://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a>*</b>

A pointer to the conditions.


### -param newCondition [out, retval]

Type: <b><a href="https://msdn.microsoft.com/66515d42-2b98-4923-b326-9fec557345b7">IUIAutomationCondition</a>**</b>

Receives a pointer to the combined condition.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method calls <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a> on each pointer in the <i>conditions</i> array. This means you can call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> on those pointers after the call to <b>CreateOrConditionFromArray</b> returns  without invalidating the pointer returned from <b>CreateOrConditionFromArray</b>. When you call <b>Release</b> on the pointer returned from  <b>CreateOrConditionFromArray</b>, UI Automation calls <b>Release</b> on each pointer in the <i>conditions</i> array.




## -see-also




<a href="https://msdn.microsoft.com/07e87cfd-d565-41b5-a68d-b99dd191fa95">Best Practices for Using Safe Arrays</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/17e83b94-21f0-44b6-87be-3fc44b0dc5a0">CreateOrCondition</a>



<a href="https://msdn.microsoft.com/393c777c-f262-462b-ac59-035f590bee1c">CreateOrConditionFromNativeArray</a>



<a href="https://msdn.microsoft.com/ead73c6d-7fb8-4e00-b027-5d747268af08">FindAll</a>



<a href="https://msdn.microsoft.com/acf16f88-2b68-4fd4-b715-b3a61340bdd0">FindAllBuildCache</a>



<a href="https://msdn.microsoft.com/84098431-46e8-49bd-a258-337ad1d68f91">FindFirst</a>



<a href="https://msdn.microsoft.com/ecb10fbf-ff1d-4bd0-b036-1050560d82fe">FindFirstBuildCache</a>



<a href="https://msdn.microsoft.com/46b31ab6-39aa-4df8-a421-6369c32a9605">IUIAutomation</a>



<a href="https://msdn.microsoft.com/66515d42-2b98-4923-b326-9fec557345b7">IUIAutomationCondition</a>



<b>Reference</b>
 

 

