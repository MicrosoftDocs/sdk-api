---
UID: NF:uiautomationcore.ITableProvider.GetRowHeaders
title: ITableProvider::GetRowHeaders (uiautomationcore.h)
description: Gets a collection of Microsoft UI Automation providers that represents all the row headers in a table.
helpviewer_keywords: ["GetRowHeaders","GetRowHeaders method [Windows Accessibility]","GetRowHeaders method [Windows Accessibility]","ITableProvider interface","ITableProvider interface [Windows Accessibility]","GetRowHeaders method","ITableProvider.GetRowHeaders","ITableProvider::GetRowHeaders","uiauto.uiauto_ITableProvider_GetRowHeaders","uiauto_ITableProvider_GetRowHeaders","uiautomationcore/ITableProvider::GetRowHeaders","winauto.uiauto_ITableProvider_GetRowHeaders"]
old-location: winauto\uiauto_ITableProvider_GetRowHeaders.htm
tech.root: WinAuto
ms.assetid: 586870cc-509f-4d5b-a3f6-0f85c86895cb
ms.date: 12/05/2018
ms.keywords: GetRowHeaders, GetRowHeaders method [Windows Accessibility], GetRowHeaders method [Windows Accessibility],ITableProvider interface, ITableProvider interface [Windows Accessibility],GetRowHeaders method, ITableProvider.GetRowHeaders, ITableProvider::GetRowHeaders, uiauto.uiauto_ITableProvider_GetRowHeaders, uiauto_ITableProvider_GetRowHeaders, uiautomationcore/ITableProvider::GetRowHeaders, winauto.uiauto_ITableProvider_GetRowHeaders
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
 - ITableProvider::GetRowHeaders
 - uiautomationcore/ITableProvider::GetRowHeaders
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
 - ITableProvider.GetRowHeaders
---

# ITableProvider::GetRowHeaders


## -description

Gets a collection of Microsoft UI Automation providers 
        that represents all the row headers in a table.

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



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itableprovider">ITableProvider</a>



<b>Reference</b>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>