---
UID: NF:uiautomationclient.IUIAutomationProxyFactoryMapping.InsertEntries
title: IUIAutomationProxyFactoryMapping::InsertEntries
author: windows-sdk-content
description: Inserts entries into the table of proxy factories.
old-location: winauto\uiauto_IUIAutomationProxyFactoryMapping_InsertEntries.htm
tech.root: WinAuto
ms.assetid: f398a1b5-d558-4187-9ee5-147b139d99e0
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IUIAutomationProxyFactoryMapping interface [Windows Accessibility],InsertEntries method, IUIAutomationProxyFactoryMapping.InsertEntries, IUIAutomationProxyFactoryMapping::InsertEntries, InsertEntries, InsertEntries method [Windows Accessibility], InsertEntries method [Windows Accessibility],IUIAutomationProxyFactoryMapping interface, uiauto.uiauto_IUIAutomationProxyFactoryMapping_InsertEntries, uiauto_IUIAutomationProxyFactoryMapping_InsertEntries, uiautomationclient/IUIAutomationProxyFactoryMapping::InsertEntries, winauto.uiauto_IUIAutomationProxyFactoryMapping_InsertEntries
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
 - IUIAutomationProxyFactoryMapping.InsertEntries
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationProxyFactoryMapping::InsertEntries


## -description


Inserts entries into the table of proxy factories.


## -parameters




### -param before [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The zero-based index at which to insert the entries.


### -param factoryList [in]

Type: <b><a href="https://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a>*</b>

A pointer to the entries to insert into the table.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/07e87cfd-d565-41b5-a68d-b99dd191fa95">Best Practices for Using Safe Arrays</a>



<a href="https://msdn.microsoft.com/7a938c1c-a11c-4fdd-a73a-e7656032f21e">IUIAutomationProxyFactoryMapping</a>
 

 

