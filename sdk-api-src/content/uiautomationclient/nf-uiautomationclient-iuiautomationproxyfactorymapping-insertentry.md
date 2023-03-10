---
UID: NF:uiautomationclient.IUIAutomationProxyFactoryMapping.InsertEntry
title: IUIAutomationProxyFactoryMapping::InsertEntry (uiautomationclient.h)
description: Insert an entry into the table of proxy factories.
helpviewer_keywords: ["IUIAutomationProxyFactoryMapping interface [Windows Accessibility]","InsertEntry method","IUIAutomationProxyFactoryMapping.InsertEntry","IUIAutomationProxyFactoryMapping::InsertEntry","InsertEntry","InsertEntry method [Windows Accessibility]","InsertEntry method [Windows Accessibility]","IUIAutomationProxyFactoryMapping interface","uiauto.uiauto_IUIAutomationProxyFactoryMapping_InsertEntry","uiauto_IUIAutomationProxyFactoryMapping_InsertEntry","uiautomationclient/IUIAutomationProxyFactoryMapping::InsertEntry","winauto.uiauto_IUIAutomationProxyFactoryMapping_InsertEntry"]
old-location: winauto\uiauto_IUIAutomationProxyFactoryMapping_InsertEntry.htm
tech.root: WinAuto
ms.assetid: fe737909-0331-4c5f-8d38-8dce09bd2e44
ms.date: 12/05/2018
ms.keywords: IUIAutomationProxyFactoryMapping interface [Windows Accessibility],InsertEntry method, IUIAutomationProxyFactoryMapping.InsertEntry, IUIAutomationProxyFactoryMapping::InsertEntry, InsertEntry, InsertEntry method [Windows Accessibility], InsertEntry method [Windows Accessibility],IUIAutomationProxyFactoryMapping interface, uiauto.uiauto_IUIAutomationProxyFactoryMapping_InsertEntry, uiauto_IUIAutomationProxyFactoryMapping_InsertEntry, uiautomationclient/IUIAutomationProxyFactoryMapping::InsertEntry, winauto.uiauto_IUIAutomationProxyFactoryMapping_InsertEntry
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
 - IUIAutomationProxyFactoryMapping::InsertEntry
 - uiautomationclient/IUIAutomationProxyFactoryMapping::InsertEntry
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
 - IUIAutomationProxyFactoryMapping.InsertEntry
---

# IUIAutomationProxyFactoryMapping::InsertEntry


## -description

Insert an entry into the table of proxy factories.

## -parameters

### -param before [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The zero-based index at which to insert the entry.

### -param factory [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationproxyfactoryentry">IUIAutomationProxyFactoryEntry</a>*</b>

The address of the entry to insert.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.