---
UID: NF:uiautomationclient.IUIAutomation.CreateNotCondition
title: IUIAutomation::CreateNotCondition
author: windows-sdk-content
description: Creates a condition that is the negative of a specified condition.
old-location: winauto\uiauto_IUIAutomation_CreateNotCondition.htm
tech.root: WinAuto
ms.assetid: 183603f9-6e5b-4c44-b6b2-c363b4d150c3
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: CreateNotCondition, CreateNotCondition method [Windows Accessibility], CreateNotCondition method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],CreateNotCondition method, IUIAutomation.CreateNotCondition, IUIAutomation::CreateNotCondition, uiauto.uiauto_IUIAutomation_CreateNotCondition, uiauto_IUIAutomation_CreateNotCondition, uiautomationclient/IUIAutomation::CreateNotCondition, winauto.uiauto_IUIAutomation_CreateNotCondition
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
 - IUIAutomation.CreateNotCondition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomation::CreateNotCondition


## -description


Creates a condition that is the negative of a specified condition.


## -parameters




### -param condition [in]

Type: <b><a href="https://msdn.microsoft.com/66515d42-2b98-4923-b326-9fec557345b7">IUIAutomationCondition</a>*</b>

A pointer to the initial condition. 


### -param newCondition [out, retval]

Type: <b><a href="https://msdn.microsoft.com/66515d42-2b98-4923-b326-9fec557345b7">IUIAutomationCondition</a>**</b>

Receives a pointer to the negative of the initial condition specified by the <i>condition</i> parameter.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <b>CreateNotCondition</b> method calls <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a> on the <i>condition</i> pointer. This means you can call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> on that pointer after the call to <b>CreateNotCondition</b> returns  without invalidating the pointer returned from <b>CreateNotCondition</b>. When you call <b>Release</b> on the pointer returned from  <b>CreateNotCondition</b>, UI Automation calls <b>Release</b> on the <i>condition</i> pointer.




## -see-also




<a href="https://msdn.microsoft.com/ead73c6d-7fb8-4e00-b027-5d747268af08">FindAll</a>



<a href="https://msdn.microsoft.com/acf16f88-2b68-4fd4-b715-b3a61340bdd0">FindAllBuildCache</a>



<a href="https://msdn.microsoft.com/84098431-46e8-49bd-a258-337ad1d68f91">FindFirst</a>



<a href="https://msdn.microsoft.com/ecb10fbf-ff1d-4bd0-b036-1050560d82fe">FindFirstBuildCache</a>



<a href="https://msdn.microsoft.com/46b31ab6-39aa-4df8-a421-6369c32a9605">IUIAutomation</a>



<a href="https://msdn.microsoft.com/66515d42-2b98-4923-b326-9fec557345b7">IUIAutomationCondition</a>



<b>Reference</b>
 

 

