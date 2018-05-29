---
UID: NF:uiautomationclient.IUIAutomationLegacyIAccessiblePattern.GetCachedSelection
title: IUIAutomationLegacyIAccessiblePattern::GetCachedSelection
author: windows-sdk-content
description: Retrieves the cached Microsoft Active Accessibility property that identifies the selected children of this element.
old-location: winauto\uiauto_IUIAutomationLegacyIAccessiblePattern_GetCachedSelection.htm
old-project: WinAuto
ms.assetid: 923c3f64-7205-4d41-b726-90324e65661e
ms.author: windowssdkdev
ms.date: 04/16/2018
ms.keywords: GetCachedSelection, GetCachedSelection method [Windows Accessibility], GetCachedSelection method [Windows Accessibility],IUIAutomationLegacyIAccessiblePattern interface, IUIAutomationLegacyIAccessiblePattern interface [Windows Accessibility],GetCachedSelection method, IUIAutomationLegacyIAccessiblePattern.GetCachedSelection, IUIAutomationLegacyIAccessiblePattern::GetCachedSelection, uiauto.uiauto_IUIAutomationLegacyIAccessiblePattern_GetCachedSelection, uiauto_IUIAutomationLegacyIAccessiblePattern_GetCachedSelection, uiautomationclient/IUIAutomationLegacyIAccessiblePattern::GetCachedSelection, winauto.uiauto_IUIAutomationLegacyIAccessiblePattern_GetCachedSelection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
-	IUIAutomationLegacyIAccessiblePattern.GetCachedSelection
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationLegacyIAccessiblePattern::GetCachedSelection


## -description


Retrieves the cached Microsoft Active Accessibility property that identifies the selected children of this element.


## -parameters




### -param pvarSelectedChildren [out, retval]

Type: <b><a href="https://msdn.microsoft.com/7ecf585c-ff3b-4f89-8a7d-e2de66650ab4">IUIAutomationElementArray</a>**</b>

Receives a pointer to the cached collection of the selected child elements.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d6564d14-a739-47bf-9202-0757ac3ba7f8">IUIAutomationLegacyIAccessiblePattern</a>
 

 

