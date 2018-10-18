---
UID: NF:uiautomationclient.IUIAutomation.CreateProxyFactoryEntry
title: IUIAutomation::CreateProxyFactoryEntry
author: windows-sdk-content
description: Creates a new instance of a proxy factory object.
old-location: winauto\uiauto_IUIAutomation_CreateProxyFactoryEntry.htm
tech.root: WinAuto
ms.assetid: dcb7ceb8-d794-4b7a-97ed-d7fc2002d7d7
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: CreateProxyFactoryEntry, CreateProxyFactoryEntry method [Windows Accessibility], CreateProxyFactoryEntry method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],CreateProxyFactoryEntry method, IUIAutomation.CreateProxyFactoryEntry, IUIAutomation::CreateProxyFactoryEntry, uiauto.uiauto_IUIAutomation_CreateProxyFactoryEntry, uiauto_IUIAutomation_CreateProxyFactoryEntry, uiautomationclient/IUIAutomation::CreateProxyFactoryEntry, winauto.uiauto_IUIAutomation_CreateProxyFactoryEntry
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
 - IUIAutomation.CreateProxyFactoryEntry
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomation::CreateProxyFactoryEntry


## -description


Creates a new instance of a proxy factory object.


## -parameters




### -param factory [in]

Type: <b><a href="https://msdn.microsoft.com/cdb2c94e-a5a7-41c3-b847-b23ea077abd3">IUIAutomationProxyFactory</a>*</b>

A pointer to  the proxy factory object.


### -param factoryEntry [out, retval]

Type: <b><a href="https://msdn.microsoft.com/0507deef-35dc-45bb-a7c1-82b84344ee17">IUIAutomationProxyFactoryEntry</a>**</b>

Receives a pointer to the newly created instance of the proxy factory object.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Use the <a href="https://msdn.microsoft.com/7a938c1c-a11c-4fdd-a73a-e7656032f21e">IUIAutomationProxyFactoryMapping</a> interface to enter the proxy factory into the table of available proxies. 




## -see-also




<a href="https://msdn.microsoft.com/46b31ab6-39aa-4df8-a421-6369c32a9605">IUIAutomation</a>
 

 

