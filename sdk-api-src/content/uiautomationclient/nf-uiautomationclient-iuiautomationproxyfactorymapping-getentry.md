---
UID: NF:uiautomationclient.IUIAutomationProxyFactoryMapping.GetEntry
title: IUIAutomationProxyFactoryMapping::GetEntry (uiautomationclient.h)
description: Retrieves an entry from the proxy factory table.
helpviewer_keywords: ["GetEntry","GetEntry method [Windows Accessibility]","GetEntry method [Windows Accessibility]","IUIAutomationProxyFactoryMapping interface","IUIAutomationProxyFactoryMapping interface [Windows Accessibility]","GetEntry method","IUIAutomationProxyFactoryMapping.GetEntry","IUIAutomationProxyFactoryMapping::GetEntry","uiauto.uiauto_IUIAutomationProxyFactoryMapping_GetEntry","uiauto_IUIAutomationProxyFactoryMapping_GetEntry","uiautomationclient/IUIAutomationProxyFactoryMapping::GetEntry","winauto.uiauto_IUIAutomationProxyFactoryMapping_GetEntry"]
old-location: winauto\uiauto_IUIAutomationProxyFactoryMapping_GetEntry.htm
tech.root: WinAuto
ms.assetid: 1500c5e5-5161-4753-ab3a-7e5b62246411
ms.date: 12/05/2018
ms.keywords: GetEntry, GetEntry method [Windows Accessibility], GetEntry method [Windows Accessibility],IUIAutomationProxyFactoryMapping interface, IUIAutomationProxyFactoryMapping interface [Windows Accessibility],GetEntry method, IUIAutomationProxyFactoryMapping.GetEntry, IUIAutomationProxyFactoryMapping::GetEntry, uiauto.uiauto_IUIAutomationProxyFactoryMapping_GetEntry, uiauto_IUIAutomationProxyFactoryMapping_GetEntry, uiautomationclient/IUIAutomationProxyFactoryMapping::GetEntry, winauto.uiauto_IUIAutomationProxyFactoryMapping_GetEntry
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
 - IUIAutomationProxyFactoryMapping::GetEntry
 - uiautomationclient/IUIAutomationProxyFactoryMapping::GetEntry
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
 - IUIAutomationProxyFactoryMapping.GetEntry
---

# IUIAutomationProxyFactoryMapping::GetEntry


## -description

Retrieves an entry from the proxy factory table.

## -parameters

### -param index [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The zero-based index of the item to retrieve.

### -param entry [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationproxyfactoryentry">IUIAutomationProxyFactoryEntry</a>**</b>

Receives a pointer to the entry.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.