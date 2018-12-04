---
UID: NF:uiautomationclient.IUIAutomationProxyFactoryMapping.GetEntry
title: IUIAutomationProxyFactoryMapping::GetEntry
author: windows-sdk-content
description: Retrieves an entry from the proxy factory table.
old-location: winauto\uiauto_IUIAutomationProxyFactoryMapping_GetEntry.htm
tech.root: WinAuto
ms.assetid: 1500c5e5-5161-4753-ab3a-7e5b62246411
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetEntry, GetEntry method [Windows Accessibility], GetEntry method [Windows Accessibility],IUIAutomationProxyFactoryMapping interface, IUIAutomationProxyFactoryMapping interface [Windows Accessibility],GetEntry method, IUIAutomationProxyFactoryMapping.GetEntry, IUIAutomationProxyFactoryMapping::GetEntry, uiauto.uiauto_IUIAutomationProxyFactoryMapping_GetEntry, uiauto_IUIAutomationProxyFactoryMapping_GetEntry, uiautomationclient/IUIAutomationProxyFactoryMapping::GetEntry, winauto.uiauto_IUIAutomationProxyFactoryMapping_GetEntry
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
 - IUIAutomationProxyFactoryMapping.GetEntry
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationProxyFactoryMapping::GetEntry


## -description


Retrieves an entry from the proxy factory table.


## -parameters




### -param index [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The zero-based index of the item to retrieve.


### -param entry [out, retval]

Type: <b><a href="https://msdn.microsoft.com/0507deef-35dc-45bb-a7c1-82b84344ee17">IUIAutomationProxyFactoryEntry</a>**</b>

Receives a pointer to the entry.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



