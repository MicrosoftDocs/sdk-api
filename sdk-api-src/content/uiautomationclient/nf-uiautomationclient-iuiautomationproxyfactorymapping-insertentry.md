---
UID: NF:uiautomationclient.IUIAutomationProxyFactoryMapping.InsertEntry
title: IUIAutomationProxyFactoryMapping::InsertEntry
author: windows-sdk-content
description: Insert an entry into the table of proxy factories.
old-location: winauto\uiauto_IUIAutomationProxyFactoryMapping_InsertEntry.htm
tech.root: WinAuto
ms.assetid: fe737909-0331-4c5f-8d38-8dce09bd2e44
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IUIAutomationProxyFactoryMapping interface [Windows Accessibility],InsertEntry method, IUIAutomationProxyFactoryMapping.InsertEntry, IUIAutomationProxyFactoryMapping::InsertEntry, InsertEntry, InsertEntry method [Windows Accessibility], InsertEntry method [Windows Accessibility],IUIAutomationProxyFactoryMapping interface, uiauto.uiauto_IUIAutomationProxyFactoryMapping_InsertEntry, uiauto_IUIAutomationProxyFactoryMapping_InsertEntry, uiautomationclient/IUIAutomationProxyFactoryMapping::InsertEntry, winauto.uiauto_IUIAutomationProxyFactoryMapping_InsertEntry
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
 - IUIAutomationProxyFactoryMapping.InsertEntry
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationProxyFactoryMapping::InsertEntry


## -description


Insert an entry into the table of proxy factories.


## -parameters




### -param before [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The zero-based index at which to insert the entry.


### -param factory [in]

Type: <b><a href="https://msdn.microsoft.com/0507deef-35dc-45bb-a7c1-82b84344ee17">IUIAutomationProxyFactoryEntry</a>*</b>

The address of the entry to insert.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



