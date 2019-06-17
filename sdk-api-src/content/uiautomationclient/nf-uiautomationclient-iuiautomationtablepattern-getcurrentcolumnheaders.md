---
UID: NF:uiautomationclient.IUIAutomationTablePattern.GetCurrentColumnHeaders
title: IUIAutomationTablePattern::GetCurrentColumnHeaders (uiautomationclient.h)
author: windows-sdk-content
description: Retrieves a collection of UI Automation elements representing all the column headers in a table.
old-location: winauto\uiauto_IUIAutomationTablePattern_GetCurrentColumnHeaders.htm
tech.root: WinAuto
ms.assetid: 4f31bfa6-0a4a-4cd6-9f5d-2964696d4acd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetCurrentColumnHeaders, GetCurrentColumnHeaders method [Windows Accessibility], GetCurrentColumnHeaders method [Windows Accessibility],IUIAutomationTablePattern interface, IUIAutomationTablePattern interface [Windows Accessibility],GetCurrentColumnHeaders method, IUIAutomationTablePattern.GetCurrentColumnHeaders, IUIAutomationTablePattern::GetCurrentColumnHeaders, uiauto.uiauto_IUIAutomationTablePattern_GetCurrentColumnHeaders, uiauto_IUIAutomationTablePattern_GetCurrentColumnHeaders, uiautomationclient/IUIAutomationTablePattern::GetCurrentColumnHeaders, winauto.uiauto_IUIAutomationTablePattern_GetCurrentColumnHeaders
ms.topic: method
f1_keywords: ["uiautomationclient/IUIAutomationTablePattern.GetCurrentColumnHeaders"]
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
 - IUIAutomationTablePattern.GetCurrentColumnHeaders
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomationTablePattern::GetCurrentColumnHeaders


## -description


Retrieves a collection of UI Automation elements representing all the column headers in a table.


## -parameters




### -param retVal [out, retval]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelementarray">IUIAutomationElementArray</a>**</b>

Receives a pointer to the collection of column headers. The default is an empty array.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtablepattern">IUIAutomationTablePattern</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtablepattern-getcurrentrowheaders">IUIAutomationTablePattern::GetCurrentRowHeaders</a>
 

 

