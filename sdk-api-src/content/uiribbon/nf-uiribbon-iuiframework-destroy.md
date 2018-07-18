---
UID: NF:uiribbon.IUIFramework.Destroy
title: IUIFramework::Destroy
author: windows-sdk-content
description: Terminates and releases all objects, hooks, and references for an instance of the Windows Ribbon framework.
old-location: windowsribbon\windowsribbon_iuiframework_destroy.htm
old-project: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuiframework\destroy.htm
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: Destroy, Destroy method [Windows Ribbon], Destroy method [Windows Ribbon],IUIFramework interface, IUIFramework interface [Windows Ribbon],Destroy method, IUIFramework.Destroy, IUIFramework::Destroy, scenicintent_IUIFramework_Destroy, uiribbon/IUIFramework::Destroy, windowsribbon.windowsribbon_iuiframework_destroy
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uiribbon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Uiribbon.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: UI_VIEWVERB
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mshtml.dll
api_name:
 - IUIFramework.Destroy
product: Windows
targetos: Windows
req.lib: 
req.dll: Mshtml.dll
req.irql: 
req.product: Windows UI
---

# IUIFramework::Destroy


## -description


Terminates and releases all objects, hooks, and references for an instance of the Windows Ribbon framework. 
		


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




				This method must be called once for each instance of <a href="https://msdn.microsoft.com/a9b8a30d-dd00-4088-a588-304fde97b84e">IUIFramework</a>.
			

If  <a href="https://msdn.microsoft.com/bb6525dd-7e05-40e0-bdcc-c66f31a99f46">IUIFramework::Initialize</a> was called, then <b>IUIFramework::Destroy</b> must be called to free resources and ensure proper dismantling of the framework. Failure to call <b>IUIFramework::Destroy</b> may cause a memory leak.




## -see-also




<a href="https://msdn.microsoft.com/a9b8a30d-dd00-4088-a588-304fde97b84e">IUIFramework</a>



<a href="https://msdn.microsoft.com/79d092c9-347b-4b8f-8ba4-a8f696ce6a85">Windows Ribbon Framework Samples</a>
 

 

