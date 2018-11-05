---
UID: NF:uiautomationclient.IUIAutomationTablePattern.GetCurrentRowHeaders
title: IUIAutomationTablePattern::GetCurrentRowHeaders
author: windows-sdk-content
description: Retrieves a collection of UI Automation elements representing all the row headers in a table.
old-location: winauto\uiauto_IUIAutomationTablePattern_GetCurrentRowHeaders.htm
tech.root: WinAuto
ms.assetid: 5669bdc7-a240-4c05-acf1-b1ff5e5b09fc
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetCurrentRowHeaders, GetCurrentRowHeaders method [Windows Accessibility], GetCurrentRowHeaders method [Windows Accessibility],IUIAutomationTablePattern interface, IUIAutomationTablePattern interface [Windows Accessibility],GetCurrentRowHeaders method, IUIAutomationTablePattern.GetCurrentRowHeaders, IUIAutomationTablePattern::GetCurrentRowHeaders, uiauto.uiauto_IUIAutomationTablePattern_GetCurrentRowHeaders, uiauto_IUIAutomationTablePattern_GetCurrentRowHeaders, uiautomationclient/IUIAutomationTablePattern::GetCurrentRowHeaders, winauto.uiauto_IUIAutomationTablePattern_GetCurrentRowHeaders
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
 - IUIAutomationTablePattern.GetCurrentRowHeaders
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationTablePattern::GetCurrentRowHeaders


## -description


Retrieves a collection of UI Automation elements representing all the row headers in a table.


## -parameters




### -param retVal [out, retval]

Type: <b><a href="https://msdn.microsoft.com/7ecf585c-ff3b-4f89-8a7d-e2de66650ab4">IUIAutomationElementArray</a>**</b>

Receives a pointer to the collection of row headers. The default is an empty array.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/a393b323-31f9-4f31-abdb-7a0fb7c8ab96">IUIAutomationTablePattern</a>



<a href="https://msdn.microsoft.com/4f31bfa6-0a4a-4cd6-9f5d-2964696d4acd">IUIAutomationTablePattern::GetCurrentColumnHeaders</a>
 

 

