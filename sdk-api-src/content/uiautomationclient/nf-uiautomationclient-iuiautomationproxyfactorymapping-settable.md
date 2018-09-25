---
UID: NF:uiautomationclient.IUIAutomationProxyFactoryMapping.SetTable
title: IUIAutomationProxyFactoryMapping::SetTable
author: windows-sdk-content
description: Sets the table of proxy factories.
old-location: winauto\uiauto_IUIAutomationProxyFactoryMapping_SetTable.htm
tech.root: WinAuto
ms.assetid: 8b3675a4-a4d5-40ed-bb11-7e4d50746019
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: IUIAutomationProxyFactoryMapping interface [Windows Accessibility],SetTable method, IUIAutomationProxyFactoryMapping.SetTable, IUIAutomationProxyFactoryMapping::SetTable, SetTable, SetTable method [Windows Accessibility], SetTable method [Windows Accessibility],IUIAutomationProxyFactoryMapping interface, uiauto.uiauto_IUIAutomationProxyFactoryMapping_SetTable, uiauto_IUIAutomationProxyFactoryMapping_SetTable, uiautomationclient/IUIAutomationProxyFactoryMapping::SetTable, winauto.uiauto_IUIAutomationProxyFactoryMapping_SetTable
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
 - IUIAutomationProxyFactoryMapping.SetTable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationProxyFactoryMapping::SetTable


## -description


Sets the table of proxy factories.


## -parameters




### -param factoryList [in]

Type: <b><a href="http://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a>*</b>

A pointer to the proxy factories to include in the table.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/07e87cfd-d565-41b5-a68d-b99dd191fa95">Best Practices for Using Safe Arrays</a>



<a href="https://msdn.microsoft.com/7a938c1c-a11c-4fdd-a73a-e7656032f21e">IUIAutomationProxyFactoryMapping</a>
 

 

