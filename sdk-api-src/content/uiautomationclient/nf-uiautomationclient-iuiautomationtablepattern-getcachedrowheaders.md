---
UID: NF:uiautomationclient.IUIAutomationTablePattern.GetCachedRowHeaders
title: IUIAutomationTablePattern::GetCachedRowHeaders
author: windows-sdk-content
description: Retrieves a cached collection of UI Automation elements representing all the row headers in a table.
old-location: winauto\uiauto_IUIAutomationTablePattern_GetCachedRowHeaders.htm
old-project: WinAuto
ms.assetid: 2487f6cd-5871-457d-b634-83bb6191dce2
ms.author: windowssdkdev
ms.date: 04/16/2018
ms.keywords: GetCachedRowHeaders, GetCachedRowHeaders method [Windows Accessibility], GetCachedRowHeaders method [Windows Accessibility],IUIAutomationTablePattern interface, IUIAutomationTablePattern interface [Windows Accessibility],GetCachedRowHeaders method, IUIAutomationTablePattern.GetCachedRowHeaders, IUIAutomationTablePattern::GetCachedRowHeaders, uiauto.uiauto_IUIAutomationTablePattern_GetCachedRowHeaders, uiauto_IUIAutomationTablePattern_GetCachedRowHeaders, uiautomationclient/IUIAutomationTablePattern::GetCachedRowHeaders, winauto.uiauto_IUIAutomationTablePattern_GetCachedRowHeaders
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAutomationClient.h
api_name:
-	IUIAutomationTablePattern.GetCachedRowHeaders
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationTablePattern::GetCachedRowHeaders


## -description


Retrieves a cached collection of UI Automation elements representing all the row headers in a table.


## -parameters




### -param retVal [out, retval]

Type: <b><a href="https://msdn.microsoft.com/7ecf585c-ff3b-4f89-8a7d-e2de66650ab4">IUIAutomationElementArray</a>**</b>

Receives a pointer to the collection of cached row headers. The default is an empty array.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/a393b323-31f9-4f31-abdb-7a0fb7c8ab96">IUIAutomationTablePattern</a>



<a href="https://msdn.microsoft.com/817a13b3-6de5-4473-8286-e3d728d06819">IUIAutomationTablePattern::GetCachedColumnHeaders</a>
 

 

