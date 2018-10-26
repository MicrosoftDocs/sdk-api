---
UID: NF:uiautomationclient.IUIAutomationElement.GetCachedChildren
title: IUIAutomationElement::GetCachedChildren
author: windows-sdk-content
description: Retrieves the cached child elements of this UI Automation element.
old-location: winauto\uiauto_IUIAutomationElement_GetCachedChildren.htm
tech.root: WinAuto
ms.assetid: dab24be3-0e0e-445f-a9cc-bb2733916cdc
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: GetCachedChildren, GetCachedChildren method [Windows Accessibility], GetCachedChildren method [Windows Accessibility],IUIAutomationElement interface, IUIAutomationElement interface [Windows Accessibility],GetCachedChildren method, IUIAutomationElement.GetCachedChildren, IUIAutomationElement::GetCachedChildren, uiauto.uiauto_IUIAutomationElement_GetCachedChildren, uiauto_IUIAutomationElement_GetCachedChildren, uiautomationclient/IUIAutomationElement::GetCachedChildren, winauto.uiauto_IUIAutomationElement_GetCachedChildren
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
 - IUIAutomationElement.GetCachedChildren
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationElement::GetCachedChildren


## -description


Retrieves the cached child elements of this UI Automation element. 


## -parameters




### -param children [out, retval]

Type: <b><a href="https://msdn.microsoft.com/7ecf585c-ff3b-4f89-8a7d-e2de66650ab4">IUIAutomationElementArray</a>**</b>

Receives a pointer to a collection of the cached child elements.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The view of the returned collection is determined by the TreeFilter property of the <a href="https://msdn.microsoft.com/8e5d7f6e-c4c7-4bb9-ba33-959e098ecd41">IUIAutomationCacheRequest</a> that was active when this element was obtained.

Children are cached only if the scope of the cache request included <a href="https://msdn.microsoft.com/en-us/library/Ee671699(v=VS.85).aspx">TreeScope_Subtree</a>, <a href="https://msdn.microsoft.com/en-us/library/Ee671699(v=VS.85).aspx">TreeScope_Children</a>, or <a href="https://msdn.microsoft.com/en-us/library/Ee671699(v=VS.85).aspx">TreeScope_Descendants</a>.

If the cache request specified that children were to be cached at this level, but there are no children, the value of this property is 0. However, if no request was made to cache children at this level, an attempt to retrieve the property returns an error.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/10ca955b-416a-47c0-9970-940d98132b38">GetCachedParent</a>



<a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>



<a href="https://msdn.microsoft.com/8675851a-4a72-4cbe-ab71-ed6fc891be17">Obtaining UI Automation Elements</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/f3afe258-baa7-41b5-a27e-cdc94b467d73">UI Automation Tree Overview</a>
 

 

