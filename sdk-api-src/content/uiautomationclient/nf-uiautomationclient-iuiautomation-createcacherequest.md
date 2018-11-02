---
UID: NF:uiautomationclient.IUIAutomation.CreateCacheRequest
title: IUIAutomation::CreateCacheRequest
author: windows-sdk-content
description: Creates a cache request.
old-location: winauto\uiauto_IUIAutomation_CreateCacheRequest.htm
tech.root: WinAuto
ms.assetid: e61aecac-8c08-4f83-b3e6-f4baedcb16c6
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: CreateCacheRequest, CreateCacheRequest method [Windows Accessibility], CreateCacheRequest method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],CreateCacheRequest method, IUIAutomation.CreateCacheRequest, IUIAutomation::CreateCacheRequest, uiauto.uiauto_IUIAutomation_CreateCacheRequest, uiauto_IUIAutomation_CreateCacheRequest, uiautomationclient/IUIAutomation::CreateCacheRequest, winauto.uiauto_IUIAutomation_CreateCacheRequest
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
 - IUIAutomation.CreateCacheRequest
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomation::CreateCacheRequest


## -description


Creates a cache request.


## -parameters




### -param cacheRequest [out, retval]

Type: <b><a href="https://msdn.microsoft.com/8e5d7f6e-c4c7-4bb9-ba33-959e098ecd41">IUIAutomationCacheRequest</a>**</b>

The address of a variable that receives a pointer to an <a href="https://msdn.microsoft.com/8e5d7f6e-c4c7-4bb9-ba33-959e098ecd41">IUIAutomationCacheRequest</a> interface.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



After obtaining the <a href="https://msdn.microsoft.com/8e5d7f6e-c4c7-4bb9-ba33-959e098ecd41">IUIAutomationCacheRequest</a> interface, use its methods to specify properties and control patterns to be cached when a UI Automation element is obtained. 
			




## -see-also




<a href="https://msdn.microsoft.com/948b3bb9-75a9-4197-9680-e6fe7bb86feb">Caching UI Automation Properties and Control Patterns</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/acf16f88-2b68-4fd4-b715-b3a61340bdd0">FindAllBuildCache</a>



<a href="https://msdn.microsoft.com/ecb10fbf-ff1d-4bd0-b036-1050560d82fe">FindFirstBuildCache</a>



<a href="https://msdn.microsoft.com/46b31ab6-39aa-4df8-a421-6369c32a9605">IUIAutomation</a>



<a href="https://msdn.microsoft.com/adb4afed-63b9-42b4-8a8d-673d4813bb52">IUIAutomationTreeWalker</a>



<b>Reference</b>
 

 

