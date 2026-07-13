---
UID: NF:uiautomationclient.IUIAutomationProxyFactoryMapping.InsertEntries
title: IUIAutomationProxyFactoryMapping::InsertEntries (uiautomationclient.h)
description: Inserts entries into the table of proxy factories.
helpviewer_keywords: ["IUIAutomationProxyFactoryMapping interface [Windows Accessibility]","InsertEntries method","IUIAutomationProxyFactoryMapping.InsertEntries","IUIAutomationProxyFactoryMapping::InsertEntries","InsertEntries","InsertEntries method [Windows Accessibility]","InsertEntries method [Windows Accessibility]","IUIAutomationProxyFactoryMapping interface","uiauto.uiauto_IUIAutomationProxyFactoryMapping_InsertEntries","uiauto_IUIAutomationProxyFactoryMapping_InsertEntries","uiautomationclient/IUIAutomationProxyFactoryMapping::InsertEntries","winauto.uiauto_IUIAutomationProxyFactoryMapping_InsertEntries"]
old-location: winauto\uiauto_IUIAutomationProxyFactoryMapping_InsertEntries.htm
tech.root: WinAuto
ms.assetid: f398a1b5-d558-4187-9ee5-147b139d99e0
ms.date: 12/05/2018
ms.keywords: IUIAutomationProxyFactoryMapping interface [Windows Accessibility],InsertEntries method, IUIAutomationProxyFactoryMapping.InsertEntries, IUIAutomationProxyFactoryMapping::InsertEntries, InsertEntries, InsertEntries method [Windows Accessibility], InsertEntries method [Windows Accessibility],IUIAutomationProxyFactoryMapping interface, uiauto.uiauto_IUIAutomationProxyFactoryMapping_InsertEntries, uiauto_IUIAutomationProxyFactoryMapping_InsertEntries, uiautomationclient/IUIAutomationProxyFactoryMapping::InsertEntries, winauto.uiauto_IUIAutomationProxyFactoryMapping_InsertEntries
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
 - IUIAutomationProxyFactoryMapping::InsertEntries
 - uiautomationclient/IUIAutomationProxyFactoryMapping::InsertEntries
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
 - IUIAutomationProxyFactoryMapping.InsertEntries
---

# IUIAutomationProxyFactoryMapping::InsertEntries


## -description

Inserts entries into the table of proxy factories.

## -parameters

### -param before [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The zero-based index at which to insert the entries.

### -param factoryList [in]

Type: <b><a href="/windows/win32/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a>*</b>

A pointer to the entries to insert into the table.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-workingwithsafearrays">Best Practices for Using Safe Arrays</a>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationproxyfactorymapping">IUIAutomationProxyFactoryMapping</a>