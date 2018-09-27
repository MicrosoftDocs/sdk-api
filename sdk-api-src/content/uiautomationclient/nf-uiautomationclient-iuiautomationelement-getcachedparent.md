---
UID: NF:uiautomationclient.IUIAutomationElement.GetCachedParent
title: IUIAutomationElement::GetCachedParent
author: windows-sdk-content
description: Retrieves from the cache the parent of this UI Automation element.
old-location: winauto\uiauto_IUIAutomationElement_GetCachedParent.htm
tech.root: WinAuto
ms.assetid: 10ca955b-416a-47c0-9970-940d98132b38
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: GetCachedParent, GetCachedParent method [Windows Accessibility], GetCachedParent method [Windows Accessibility],IUIAutomationElement interface, IUIAutomationElement interface [Windows Accessibility],GetCachedParent method, IUIAutomationElement.GetCachedParent, IUIAutomationElement::GetCachedParent, uiauto.uiauto_IUIAutomationElement_GetCachedParent, uiauto_IUIAutomationElement_GetCachedParent, uiautomationclient/IUIAutomationElement::GetCachedParent, winauto.uiauto_IUIAutomationElement_GetCachedParent
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
 - IUIAutomationElement.GetCachedParent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationElement::GetCachedParent


## -description


Retrieves from the cache the parent of this UI Automation element. 


## -parameters




### -param parent [out, retval]

Type: <b><a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>**</b>

Receives a pointer to the cached parent element.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/dab24be3-0e0e-445f-a9cc-bb2733916cdc">GetCachedChildren</a>



<a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>



<a href="https://msdn.microsoft.com/8675851a-4a72-4cbe-ab71-ed6fc891be17">Obtaining UI Automation Elements</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/f3afe258-baa7-41b5-a27e-cdc94b467d73">UI Automation Tree Overview</a>
 

 

