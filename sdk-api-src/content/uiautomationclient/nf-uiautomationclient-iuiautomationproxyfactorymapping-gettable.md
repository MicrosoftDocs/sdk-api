---
UID: NF:uiautomationclient.IUIAutomationProxyFactoryMapping.GetTable
title: IUIAutomationProxyFactoryMapping::GetTable (uiautomationclient.h)
description: Retrieves all entries in the proxy factory table.
helpviewer_keywords: ["GetTable","GetTable method [Windows Accessibility]","GetTable method [Windows Accessibility]","IUIAutomationProxyFactoryMapping interface","IUIAutomationProxyFactoryMapping interface [Windows Accessibility]","GetTable method","IUIAutomationProxyFactoryMapping.GetTable","IUIAutomationProxyFactoryMapping::GetTable","uiauto.uiauto_IUIAutomationProxyFactoryMapping_GetTable","uiauto_IUIAutomationProxyFactoryMapping_GetTable","uiautomationclient/IUIAutomationProxyFactoryMapping::GetTable","winauto.uiauto_IUIAutomationProxyFactoryMapping_GetTable"]
old-location: winauto\uiauto_IUIAutomationProxyFactoryMapping_GetTable.htm
tech.root: WinAuto
ms.assetid: 6e84ec4d-9589-47b0-ae69-5d640141dd8b
ms.date: 12/05/2018
ms.keywords: GetTable, GetTable method [Windows Accessibility], GetTable method [Windows Accessibility],IUIAutomationProxyFactoryMapping interface, IUIAutomationProxyFactoryMapping interface [Windows Accessibility],GetTable method, IUIAutomationProxyFactoryMapping.GetTable, IUIAutomationProxyFactoryMapping::GetTable, uiauto.uiauto_IUIAutomationProxyFactoryMapping_GetTable, uiauto_IUIAutomationProxyFactoryMapping_GetTable, uiautomationclient/IUIAutomationProxyFactoryMapping::GetTable, winauto.uiauto_IUIAutomationProxyFactoryMapping_GetTable
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
 - IUIAutomationProxyFactoryMapping::GetTable
 - uiautomationclient/IUIAutomationProxyFactoryMapping::GetTable
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
 - IUIAutomationProxyFactoryMapping.GetTable
---

# IUIAutomationProxyFactoryMapping::GetTable


## -description

Retrieves all entries in the proxy factory table.

## -parameters

### -param table [out, retval]

Type: <b><a href="/windows/win32/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a>**</b>

Receives a pointer to an array of table entries.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-workingwithsafearrays">Best Practices for Using Safe Arrays</a>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationproxyfactorymapping">IUIAutomationProxyFactoryMapping</a>