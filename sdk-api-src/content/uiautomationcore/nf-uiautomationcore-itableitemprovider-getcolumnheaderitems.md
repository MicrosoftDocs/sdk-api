---
UID: NF:uiautomationcore.ITableItemProvider.GetColumnHeaderItems
title: ITableItemProvider::GetColumnHeaderItems method
author: windows-driver-content
description: Retrieves a collection of Microsoft UI Automation provider representing all the column headers associated with a table item or cell.
old-location: winauto\uiauto_ITableItemProvider_GetColumnHeaderItems.htm
old-project: WinAuto
ms.assetid: b08e20e8-142c-4f83-8422-c0e6ae2b7ebf
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: GetColumnHeaderItems method [Windows Accessibility], GetColumnHeaderItems method [Windows Accessibility], ITableItemProvider interface, GetColumnHeaderItems,ITableItemProvider.GetColumnHeaderItems, ITableItemProvider, ITableItemProvider interface [Windows Accessibility], GetColumnHeaderItems method, ITableItemProvider::GetColumnHeaderItems, uiauto.uiauto_ITableItemProvider_GetColumnHeaderItems, uiauto_ITableItemProvider_GetColumnHeaderItems, uiautomationcore/ITableItemProvider::GetColumnHeaderItems, winauto.uiauto_ITableItemProvider_GetColumnHeaderItems
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
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
-	UIAutomationCore.h
api_name:
-	ITableItemProvider.GetColumnHeaderItems
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITableItemProvider::GetColumnHeaderItems method


## -description



        Retrieves a collection of Microsoft UI Automation provider 
        representing all the column headers associated with a table item or cell.
        


## -parameters




### -param pRetVal [out, retval]

Type: <b><a href="http://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a>**</b>

Receives a pointer to a <a href="http://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a> that contains an array of pointers to the <a href="https://msdn.microsoft.com/f0ec6185-acd0-4df7-88f4-fd00747f98bf">IRawElementProviderSimple</a> interfaces of
				the column headers. This parameter is passed uninitialized.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/07e87cfd-d565-41b5-a68d-b99dd191fa95">Best Practices for Using Safe Arrays</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/73cba491-1aa6-4bd7-bcd6-95b5d85c9457">ITableItemProvider</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

