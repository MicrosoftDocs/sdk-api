---
UID: NF:uiautomationclient.IUIAutomationElement.BuildUpdatedCache
title: IUIAutomationElement::BuildUpdatedCache (uiautomationclient.h)
author: windows-sdk-content
description: Retrieves a new UI Automation element with an updated cache.
old-location: winauto\uiauto_IUIAutomationElement_BuildUpdatedCache.htm
tech.root: WinAuto
ms.assetid: b2499b3c-433f-4e2f-937c-78da66c16203
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: BuildUpdatedCache, BuildUpdatedCache method [Windows Accessibility], BuildUpdatedCache method [Windows Accessibility],IUIAutomationElement interface, IUIAutomationElement interface [Windows Accessibility],BuildUpdatedCache method, IUIAutomationElement.BuildUpdatedCache, IUIAutomationElement::BuildUpdatedCache, uiauto.uiauto_IUIAutomationElement_BuildUpdatedCache, uiauto_IUIAutomationElement_BuildUpdatedCache, uiautomationclient/IUIAutomationElement::BuildUpdatedCache, winauto.uiauto_IUIAutomationElement_BuildUpdatedCache
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
 - IUIAutomationElement.BuildUpdatedCache
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationElement::BuildUpdatedCache


## -description


Retrieves a new UI Automation element with an updated cache.


## -parameters




### -param cacheRequest [in]

Type: <b><a href="https://msdn.microsoft.com/8e5d7f6e-c4c7-4bb9-ba33-959e098ecd41">IUIAutomationCacheRequest</a>*</b>

A pointer to a cache request that specifies the control patterns and properties to include in the cache.


### -param updatedElement [out, retval]

Type: <b><a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>**</b>

Receives a pointer to the new UI Automation element.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The original UI Automation element is unchanged. The new <a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a> interface refers to the same element and has the same runtime identifier.

			




## -see-also




<a href="https://msdn.microsoft.com/948b3bb9-75a9-4197-9680-e6fe7bb86feb">Caching UI Automation Properties and Control Patterns</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>



<b>Reference</b>
 

 

