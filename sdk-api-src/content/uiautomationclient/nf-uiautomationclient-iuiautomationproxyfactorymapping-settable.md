---
UID: NF:uiautomationclient.IUIAutomationProxyFactoryMapping.SetTable
title: IUIAutomationProxyFactoryMapping::SetTable (uiautomationclient.h)
description: Sets the table of proxy factories.
helpviewer_keywords: ["IUIAutomationProxyFactoryMapping interface [Windows Accessibility]","SetTable method","IUIAutomationProxyFactoryMapping.SetTable","IUIAutomationProxyFactoryMapping::SetTable","SetTable","SetTable method [Windows Accessibility]","SetTable method [Windows Accessibility]","IUIAutomationProxyFactoryMapping interface","uiauto.uiauto_IUIAutomationProxyFactoryMapping_SetTable","uiauto_IUIAutomationProxyFactoryMapping_SetTable","uiautomationclient/IUIAutomationProxyFactoryMapping::SetTable","winauto.uiauto_IUIAutomationProxyFactoryMapping_SetTable"]
old-location: winauto\uiauto_IUIAutomationProxyFactoryMapping_SetTable.htm
tech.root: WinAuto
ms.assetid: 8b3675a4-a4d5-40ed-bb11-7e4d50746019
ms.date: 12/05/2018
ms.keywords: IUIAutomationProxyFactoryMapping interface [Windows Accessibility],SetTable method, IUIAutomationProxyFactoryMapping.SetTable, IUIAutomationProxyFactoryMapping::SetTable, SetTable, SetTable method [Windows Accessibility], SetTable method [Windows Accessibility],IUIAutomationProxyFactoryMapping interface, uiauto.uiauto_IUIAutomationProxyFactoryMapping_SetTable, uiauto_IUIAutomationProxyFactoryMapping_SetTable, uiautomationclient/IUIAutomationProxyFactoryMapping::SetTable, winauto.uiauto_IUIAutomationProxyFactoryMapping_SetTable
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
 - IUIAutomationProxyFactoryMapping::SetTable
 - uiautomationclient/IUIAutomationProxyFactoryMapping::SetTable
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
 - IUIAutomationProxyFactoryMapping.SetTable
---

# IUIAutomationProxyFactoryMapping::SetTable


## -description

Sets the table of proxy factories.

## -parameters

### -param factoryList [in]

Type: <b><a href="/windows/win32/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a>*</b>

A pointer to the proxy factories to include in the table.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-workingwithsafearrays">Best Practices for Using Safe Arrays</a>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationproxyfactorymapping">IUIAutomationProxyFactoryMapping</a>