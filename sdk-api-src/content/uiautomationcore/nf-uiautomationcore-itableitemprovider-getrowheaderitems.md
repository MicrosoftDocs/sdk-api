---
UID: NF:uiautomationcore.ITableItemProvider.GetRowHeaderItems
title: ITableItemProvider::GetRowHeaderItems
author: windows-sdk-content
description: Retrieves a collection of Microsoft UI Automation provider representing all the row headers associated with a table item or cell.
old-location: winauto\uiauto_ITableItemProvider_GetRowHeaderItems.htm
tech.root: WinAuto
ms.assetid: 02717f9a-93dd-4963-bbc7-a1eb257bf5e5
ms.author: windowssdkdev
ms.date: 10/23/2018
ms.keywords: GetRowHeaderItems, GetRowHeaderItems method [Windows Accessibility], GetRowHeaderItems method [Windows Accessibility],ITableItemProvider interface, ITableItemProvider interface [Windows Accessibility],GetRowHeaderItems method, ITableItemProvider.GetRowHeaderItems, ITableItemProvider::GetRowHeaderItems, uiauto.uiauto_ITableItemProvider_GetRowHeaderItems, uiauto_ITableItemProvider_GetRowHeaderItems, uiautomationcore/ITableItemProvider::GetRowHeaderItems, winauto.uiauto_ITableItemProvider_GetRowHeaderItems
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ITableItemProvider.GetRowHeaderItems
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITableItemProvider::GetRowHeaderItems


## -description


Retrieves a collection of Microsoft UI Automation provider 
        representing all the row headers associated with a table item or cell.
        


## -parameters




### -param pRetVal [out, retval]

Type: <b><a href="http://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a>**</b>

Receives a pointer to a <a href="http://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a> that contains an array of pointers to the <a href="https://msdn.microsoft.com/f0ec6185-acd0-4df7-88f4-fd00747f98bf">IRawElementProviderSimple</a> interfaces
				of the row headers. This parameter is passed uninitialized.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/07e87cfd-d565-41b5-a68d-b99dd191fa95">Best Practices for Using Safe Arrays</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/73cba491-1aa6-4bd7-bcd6-95b5d85c9457">ITableItemProvider</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

