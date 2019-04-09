---
UID: NF:uiautomationcore.ITableProvider.GetColumnHeaders
title: ITableProvider::GetColumnHeaders (uiautomationcore.h)
author: windows-sdk-content
description: Gets a collection of Microsoft UI Automation providers that represents all the column headers in a table.
old-location: winauto\uiauto_ITableProvider_GetColumnHeaders.htm
tech.root: WinAuto
ms.assetid: ee7a4e40-58eb-4400-96c2-0d2196837a24
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetColumnHeaders, GetColumnHeaders method [Windows Accessibility], GetColumnHeaders method [Windows Accessibility],ITableProvider interface, ITableProvider interface [Windows Accessibility],GetColumnHeaders method, ITableProvider.GetColumnHeaders, ITableProvider::GetColumnHeaders, uiauto.uiauto_ITableProvider_GetColumnHeaders, uiauto_ITableProvider_GetColumnHeaders, uiautomationcore/ITableProvider::GetColumnHeaders, winauto.uiauto_ITableProvider_GetColumnHeaders
ms.topic: method
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
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
 - UIAutomationCore.h
api_name:
 - ITableProvider.GetColumnHeaders
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITableProvider::GetColumnHeaders


## -description


Gets a collection of Microsoft UI Automation providers 
        that represents all the column headers in a table.        
        


## -parameters




### -param pRetVal [out, retval]

Type: <b><a href="https://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a>**</b>

Receives a pointer to a <a href="https://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a> that contains an array of pointers to the <a href="https://msdn.microsoft.com/f0ec6185-acd0-4df7-88f4-fd00747f98bf">IRawElementProviderSimple</a> interfaces
				of the column headers. This parameter is passed uninitialized.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/07e87cfd-d565-41b5-a68d-b99dd191fa95">Best Practices for Using Safe Arrays</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/ae6be8be-78ea-4843-924f-2dc5d5286da2">ITableProvider</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

