---
UID: NF:uiautomationcore.ITableItemProvider.GetRowHeaderItems
title: ITableItemProvider::GetRowHeaderItems (uiautomationcore.h)
description: Retrieves a collection of Microsoft UI Automation provider representing all the row headers associated with a table item or cell.
helpviewer_keywords: ["GetRowHeaderItems","GetRowHeaderItems method [Windows Accessibility]","GetRowHeaderItems method [Windows Accessibility]","ITableItemProvider interface","ITableItemProvider interface [Windows Accessibility]","GetRowHeaderItems method","ITableItemProvider.GetRowHeaderItems","ITableItemProvider::GetRowHeaderItems","uiauto.uiauto_ITableItemProvider_GetRowHeaderItems","uiauto_ITableItemProvider_GetRowHeaderItems","uiautomationcore/ITableItemProvider::GetRowHeaderItems","winauto.uiauto_ITableItemProvider_GetRowHeaderItems"]
old-location: winauto\uiauto_ITableItemProvider_GetRowHeaderItems.htm
tech.root: WinAuto
ms.assetid: 02717f9a-93dd-4963-bbc7-a1eb257bf5e5
ms.date: 12/05/2018
ms.keywords: GetRowHeaderItems, GetRowHeaderItems method [Windows Accessibility], GetRowHeaderItems method [Windows Accessibility],ITableItemProvider interface, ITableItemProvider interface [Windows Accessibility],GetRowHeaderItems method, ITableItemProvider.GetRowHeaderItems, ITableItemProvider::GetRowHeaderItems, uiauto.uiauto_ITableItemProvider_GetRowHeaderItems, uiauto_ITableItemProvider_GetRowHeaderItems, uiautomationcore/ITableItemProvider::GetRowHeaderItems, winauto.uiauto_ITableItemProvider_GetRowHeaderItems
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
 - ITableItemProvider::GetRowHeaderItems
 - uiautomationcore/ITableItemProvider::GetRowHeaderItems
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
 - ITableItemProvider.GetRowHeaderItems
---

# ITableItemProvider::GetRowHeaderItems


## -description

Retrieves a collection of Microsoft UI Automation provider 
        representing all the row headers associated with a table item or cell.

## -parameters

### -param pRetVal [out, retval]

Type: <b><a href="/windows/win32/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a>**</b>

Receives a pointer to a <a href="/windows/win32/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> that contains an array of pointers to the <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementprovidersimple">IRawElementProviderSimple</a> interfaces
				of the row headers. This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-workingwithsafearrays">Best Practices for Using Safe Arrays</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itableitemprovider">ITableItemProvider</a>



<b>Reference</b>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>