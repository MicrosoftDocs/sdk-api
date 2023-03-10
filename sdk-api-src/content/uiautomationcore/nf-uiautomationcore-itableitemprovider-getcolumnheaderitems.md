---
UID: NF:uiautomationcore.ITableItemProvider.GetColumnHeaderItems
title: ITableItemProvider::GetColumnHeaderItems (uiautomationcore.h)
description: Retrieves a collection of Microsoft UI Automation provider representing all the column headers associated with a table item or cell.
helpviewer_keywords: ["GetColumnHeaderItems","GetColumnHeaderItems method [Windows Accessibility]","GetColumnHeaderItems method [Windows Accessibility]","ITableItemProvider interface","ITableItemProvider interface [Windows Accessibility]","GetColumnHeaderItems method","ITableItemProvider.GetColumnHeaderItems","ITableItemProvider::GetColumnHeaderItems","uiauto.uiauto_ITableItemProvider_GetColumnHeaderItems","uiauto_ITableItemProvider_GetColumnHeaderItems","uiautomationcore/ITableItemProvider::GetColumnHeaderItems","winauto.uiauto_ITableItemProvider_GetColumnHeaderItems"]
old-location: winauto\uiauto_ITableItemProvider_GetColumnHeaderItems.htm
tech.root: WinAuto
ms.assetid: b08e20e8-142c-4f83-8422-c0e6ae2b7ebf
ms.date: 12/05/2018
ms.keywords: GetColumnHeaderItems, GetColumnHeaderItems method [Windows Accessibility], GetColumnHeaderItems method [Windows Accessibility],ITableItemProvider interface, ITableItemProvider interface [Windows Accessibility],GetColumnHeaderItems method, ITableItemProvider.GetColumnHeaderItems, ITableItemProvider::GetColumnHeaderItems, uiauto.uiauto_ITableItemProvider_GetColumnHeaderItems, uiauto_ITableItemProvider_GetColumnHeaderItems, uiautomationcore/ITableItemProvider::GetColumnHeaderItems, winauto.uiauto_ITableItemProvider_GetColumnHeaderItems
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
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
 - ITableItemProvider::GetColumnHeaderItems
 - uiautomationcore/ITableItemProvider::GetColumnHeaderItems
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.h
api_name:
 - ITableItemProvider.GetColumnHeaderItems
---

# ITableItemProvider::GetColumnHeaderItems


## -description

Retrieves a collection of Microsoft UI Automation provider 
        representing all the column headers associated with a table item or cell.

## -parameters

### -param pRetVal [out, retval]

Type: <b><a href="/windows/win32/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a>**</b>

Receives a pointer to a <a href="/windows/win32/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> that contains an array of pointers to the <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementprovidersimple">IRawElementProviderSimple</a> interfaces of
				the column headers. This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-workingwithsafearrays">Best Practices for Using Safe Arrays</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itableitemprovider">ITableItemProvider</a>



<b>Reference</b>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>