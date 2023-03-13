---
UID: NF:uiautomationclient.IUIAutomationCacheRequest.get_AutomationElementMode
title: IUIAutomationCacheRequest::get_AutomationElementMode (uiautomationclient.h)
description: Indicates whether returned elements contain full references to the underlying UI, or only cached information. (Get)
helpviewer_keywords: ["AutomationElementMode property [Windows Accessibility]","AutomationElementMode property [Windows Accessibility]","IUIAutomationCacheRequest interface","IUIAutomationCacheRequest interface [Windows Accessibility]","AutomationElementMode property","IUIAutomationCacheRequest.AutomationElementMode","IUIAutomationCacheRequest.get_AutomationElementMode","IUIAutomationCacheRequest::AutomationElementMode","IUIAutomationCacheRequest::get_AutomationElementMode","IUIAutomationCacheRequest::put_AutomationElementMode","get_AutomationElementMode","uiauto.uiauto_IUIAutomationCacheRequest_AutomationElementMode","uiauto_IUIAutomationCacheRequest_AutomationElementMode","uiautomationclient/IUIAutomationCacheRequest::AutomationElementMode","uiautomationclient/IUIAutomationCacheRequest::get_AutomationElementMode","uiautomationclient/IUIAutomationCacheRequest::put_AutomationElementMode","winauto.uiauto_IUIAutomationCacheRequest_AutomationElementMode"]
old-location: winauto\uiauto_IUIAutomationCacheRequest_AutomationElementMode.htm
tech.root: WinAuto
ms.assetid: dd4c6407-d14e-4e67-9681-1f90741da38e
ms.date: 12/05/2018
ms.keywords: AutomationElementMode property [Windows Accessibility], AutomationElementMode property [Windows Accessibility],IUIAutomationCacheRequest interface, IUIAutomationCacheRequest interface [Windows Accessibility],AutomationElementMode property, IUIAutomationCacheRequest.AutomationElementMode, IUIAutomationCacheRequest.get_AutomationElementMode, IUIAutomationCacheRequest::AutomationElementMode, IUIAutomationCacheRequest::get_AutomationElementMode, IUIAutomationCacheRequest::put_AutomationElementMode, get_AutomationElementMode, uiauto.uiauto_IUIAutomationCacheRequest_AutomationElementMode, uiauto_IUIAutomationCacheRequest_AutomationElementMode, uiautomationclient/IUIAutomationCacheRequest::AutomationElementMode, uiautomationclient/IUIAutomationCacheRequest::get_AutomationElementMode, uiautomationclient/IUIAutomationCacheRequest::put_AutomationElementMode, winauto.uiauto_IUIAutomationCacheRequest_AutomationElementMode
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAutomationCacheRequest::get_AutomationElementMode
 - uiautomationclient/IUIAutomationCacheRequest::get_AutomationElementMode
dev_langs:
 - c++
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
---

# IUIAutomationCacheRequest::get_AutomationElementMode


## -description

Indicates whether returned elements contain full references to the underlying UI, or only cached information. 

This property is read/write.

## -parameters

## -remarks

<a href="/windows/desktop/api/uiautomationclient/ne-uiautomationclient-automationelementmode">AutomationElementMode_Full</a> is the default value, and specifies that returned elements contain a full reference to the underlying UI. <a href="/windows/desktop/api/uiautomationclient/ne-uiautomationclient-automationelementmode">AutomationElementMode_None</a> specifies that the returned elements have no reference to the underlying UI, and contain only cached information.

Certain operations on elements, including <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue">GetCurrentPropertyValue</a>, and <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-setfocus">SetFocus</a>, require a full reference; attempting to perform these on an element that has none results in an error.

Using <a href="/windows/desktop/api/uiautomationclient/ne-uiautomationclient-automationelementmode">AutomationElementMode_None</a> can be more efficient when only properties are needed, as it avoids the overhead involved in setting up full references.
