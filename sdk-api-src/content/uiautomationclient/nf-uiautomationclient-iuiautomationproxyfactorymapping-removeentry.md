---
UID: NF:uiautomationclient.IUIAutomationProxyFactoryMapping.RemoveEntry
title: IUIAutomationProxyFactoryMapping::RemoveEntry (uiautomationclient.h)
description: Removes an entry from the table of proxy factories.
helpviewer_keywords: ["IUIAutomationProxyFactoryMapping interface [Windows Accessibility]","RemoveEntry method","IUIAutomationProxyFactoryMapping.RemoveEntry","IUIAutomationProxyFactoryMapping::RemoveEntry","RemoveEntry","RemoveEntry method [Windows Accessibility]","RemoveEntry method [Windows Accessibility]","IUIAutomationProxyFactoryMapping interface","uiauto.uiauto_IUIAutomationProxyFactoryMapping_RemoveEntry","uiauto_IUIAutomationProxyFactoryMapping_RemoveEntry","uiautomationclient/IUIAutomationProxyFactoryMapping::RemoveEntry","winauto.uiauto_IUIAutomationProxyFactoryMapping_RemoveEntry"]
old-location: winauto\uiauto_IUIAutomationProxyFactoryMapping_RemoveEntry.htm
tech.root: WinAuto
ms.assetid: 1a09fbda-9e95-4f31-b669-e68310071aa9
ms.date: 12/05/2018
ms.keywords: IUIAutomationProxyFactoryMapping interface [Windows Accessibility],RemoveEntry method, IUIAutomationProxyFactoryMapping.RemoveEntry, IUIAutomationProxyFactoryMapping::RemoveEntry, RemoveEntry, RemoveEntry method [Windows Accessibility], RemoveEntry method [Windows Accessibility],IUIAutomationProxyFactoryMapping interface, uiauto.uiauto_IUIAutomationProxyFactoryMapping_RemoveEntry, uiauto_IUIAutomationProxyFactoryMapping_RemoveEntry, uiautomationclient/IUIAutomationProxyFactoryMapping::RemoveEntry, winauto.uiauto_IUIAutomationProxyFactoryMapping_RemoveEntry
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAutomationProxyFactoryMapping::RemoveEntry
 - uiautomationclient/IUIAutomationProxyFactoryMapping::RemoveEntry
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomationProxyFactoryMapping.RemoveEntry
---

# IUIAutomationProxyFactoryMapping::RemoveEntry


## -description

Removes an entry from the table of proxy factories.

## -parameters

### -param index [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The zero-based index of the entry to remove.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.