---
UID: NF:uiautomationclient.IUIAutomationCacheRequest.get_AutomationElementMode
title: IUIAutomationCacheRequest::get_AutomationElementMode
author: windows-sdk-content
description: Indicates whether returned elements contain full references to the underlying UI, or only cached information.
old-location: winauto\uiauto_IUIAutomationCacheRequest_AutomationElementMode.htm
old-project: WinAuto
ms.assetid: dd4c6407-d14e-4e67-9681-1f90741da38e
ms.author: windowssdkdev
ms.date: 04/16/2018
ms.keywords: AutomationElementMode property [Windows Accessibility], AutomationElementMode property [Windows Accessibility],IUIAutomationCacheRequest interface, IUIAutomationCacheRequest interface [Windows Accessibility],AutomationElementMode property, IUIAutomationCacheRequest.AutomationElementMode, IUIAutomationCacheRequest.get_AutomationElementMode, IUIAutomationCacheRequest::AutomationElementMode, IUIAutomationCacheRequest::get_AutomationElementMode, IUIAutomationCacheRequest::put_AutomationElementMode, get_AutomationElementMode, uiauto.uiauto_IUIAutomationCacheRequest_AutomationElementMode, uiauto_IUIAutomationCacheRequest_AutomationElementMode, uiautomationclient/IUIAutomationCacheRequest::AutomationElementMode, uiautomationclient/IUIAutomationCacheRequest::get_AutomationElementMode, uiautomationclient/IUIAutomationCacheRequest::put_AutomationElementMode, winauto.uiauto_IUIAutomationCacheRequest_AutomationElementMode
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
 - IUIAutomationCacheRequest.AutomationElementMode
 - IUIAutomationCacheRequest.get_AutomationElementMode
 - IUIAutomationCacheRequest.put_AutomationElementMode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationCacheRequest::get_AutomationElementMode


## -description


Indicates whether returned elements contain full references to the underlying UI, or only cached information. 

This property is read/write.


## -parameters


## -remarks



<a href="uiauto_AutomationElementModeEnum.htm">AutomationElementMode_Full</a> is the default value, and specifies that returned elements contain a full reference to the underlying UI. <a href="uiauto_AutomationElementModeEnum.htm">AutomationElementMode_None</a> specifies that the returned elements have no reference to the underlying UI, and contain only cached information.

Certain operations on elements, including <a href="https://msdn.microsoft.com/819e548e-7ff4-4f9f-969b-bfd1625f6151">GetCurrentPropertyValue</a>, and <a href="https://msdn.microsoft.com/4a4e549a-1812-4380-bc0a-2da579a62b5d">SetFocus</a>, require a full reference; attempting to perform these on an element that has none results in an error.

Using <a href="uiauto_AutomationElementModeEnum.htm">AutomationElementMode_None</a> can be more efficient when only properties are needed, as it avoids the overhead involved in setting up full references.



