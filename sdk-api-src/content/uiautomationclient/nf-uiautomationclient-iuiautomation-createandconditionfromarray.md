---
UID: NF:uiautomationclient.IUIAutomation.CreateAndConditionFromArray
title: IUIAutomation::CreateAndConditionFromArray
author: windows-sdk-content
description: Creates a condition that selects elements based on multiple conditions, all of which must be true.
old-location: winauto\uiauto_IUIAutomation_CreateAndConditionFromArray.htm
old-project: WinAuto
ms.assetid: ec9ad1a1-72c7-4fc6-8812-577b44b4c5eb
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: CreateAndConditionFromArray, CreateAndConditionFromArray method [Windows Accessibility], CreateAndConditionFromArray method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],CreateAndConditionFromArray method, IUIAutomation.CreateAndConditionFromArray, IUIAutomation::CreateAndConditionFromArray, uiauto.uiauto_IUIAutomation_CreateAndConditionFromArray, uiauto_IUIAutomation_CreateAndConditionFromArray, uiautomationclient/IUIAutomation::CreateAndConditionFromArray, winauto.uiauto_IUIAutomation_CreateAndConditionFromArray
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
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomation.CreateAndConditionFromArray
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomation::CreateAndConditionFromArray


## -description


Creates a condition that selects elements based on multiple conditions, all of which must be true.


## -parameters




### -param conditions [in]

Type: <b><a href="http://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a>*</b>

A pointer to the conditions to be combined.


### -param newCondition [out, retval]

Type: <b><a href="https://msdn.microsoft.com/66515d42-2b98-4923-b326-9fec557345b7">IUIAutomationCondition</a>**</b>

Receives a pointer to the combined condition.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method calls <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a> on each pointer in the <i>conditions</i> array. This means you can call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> on those pointers after the call to <b>CreateAndConditionFromArray</b> returns  without invalidating the pointer returned from <b>CreateAndConditionFromArray</b>. When you call <b>Release</b> on the pointer returned from  <b>CreateAndConditionFromArray</b>, UI Automation calls <b>Release</b> on each pointer in the <i>conditions</i> array.




## -see-also




<a href="https://msdn.microsoft.com/07e87cfd-d565-41b5-a68d-b99dd191fa95">Best Practices for Using Safe Arrays</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/066476b4-586c-477c-82ee-de2f2074d63b">CreateAndCondition</a>



<a href="https://msdn.microsoft.com/2f47dfa7-1558-4984-8400-cac549543819">CreateAndConditionFromNativeArray</a>



<a href="https://msdn.microsoft.com/ead73c6d-7fb8-4e00-b027-5d747268af08">FindAll</a>



<a href="https://msdn.microsoft.com/acf16f88-2b68-4fd4-b715-b3a61340bdd0">FindAllBuildCache</a>



<a href="https://msdn.microsoft.com/84098431-46e8-49bd-a258-337ad1d68f91">FindFirst</a>



<a href="https://msdn.microsoft.com/ecb10fbf-ff1d-4bd0-b036-1050560d82fe">FindFirstBuildCache</a>



<a href="https://msdn.microsoft.com/46b31ab6-39aa-4df8-a421-6369c32a9605">IUIAutomation</a>



<a href="https://msdn.microsoft.com/66515d42-2b98-4923-b326-9fec557345b7">IUIAutomationCondition</a>



<b>Reference</b>
 

 

