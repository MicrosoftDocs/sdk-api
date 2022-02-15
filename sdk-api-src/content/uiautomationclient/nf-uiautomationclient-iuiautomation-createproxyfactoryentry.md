---
UID: NF:uiautomationclient.IUIAutomation.CreateProxyFactoryEntry
title: IUIAutomation::CreateProxyFactoryEntry (uiautomationclient.h)
description: Creates a new instance of a proxy factory object.
helpviewer_keywords: ["CreateProxyFactoryEntry","CreateProxyFactoryEntry method [Windows Accessibility]","CreateProxyFactoryEntry method [Windows Accessibility]","IUIAutomation interface","IUIAutomation interface [Windows Accessibility]","CreateProxyFactoryEntry method","IUIAutomation.CreateProxyFactoryEntry","IUIAutomation::CreateProxyFactoryEntry","uiauto.uiauto_IUIAutomation_CreateProxyFactoryEntry","uiauto_IUIAutomation_CreateProxyFactoryEntry","uiautomationclient/IUIAutomation::CreateProxyFactoryEntry","winauto.uiauto_IUIAutomation_CreateProxyFactoryEntry"]
old-location: winauto\uiauto_IUIAutomation_CreateProxyFactoryEntry.htm
tech.root: WinAuto
ms.assetid: dcb7ceb8-d794-4b7a-97ed-d7fc2002d7d7
ms.date: 12/05/2018
ms.keywords: CreateProxyFactoryEntry, CreateProxyFactoryEntry method [Windows Accessibility], CreateProxyFactoryEntry method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],CreateProxyFactoryEntry method, IUIAutomation.CreateProxyFactoryEntry, IUIAutomation::CreateProxyFactoryEntry, uiauto.uiauto_IUIAutomation_CreateProxyFactoryEntry, uiauto_IUIAutomation_CreateProxyFactoryEntry, uiautomationclient/IUIAutomation::CreateProxyFactoryEntry, winauto.uiauto_IUIAutomation_CreateProxyFactoryEntry
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
 - IUIAutomation::CreateProxyFactoryEntry
 - uiautomationclient/IUIAutomation::CreateProxyFactoryEntry
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
 - IUIAutomation.CreateProxyFactoryEntry
---

# IUIAutomation::CreateProxyFactoryEntry


## -description

Creates a new instance of a proxy factory object.

## -parameters

### -param factory [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationproxyfactory">IUIAutomationProxyFactory</a>*</b>

A pointer to  the proxy factory object.

### -param factoryEntry [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationproxyfactoryentry">IUIAutomationProxyFactoryEntry</a>**</b>

Receives a pointer to the newly created instance of the proxy factory object.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Use the <a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationproxyfactorymapping">IUIAutomationProxyFactoryMapping</a> interface to enter the proxy factory into the table of available proxies.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation">IUIAutomation</a>