---
UID: NF:uiautomationcore.IMultipleViewProvider.GetSupportedViews
title: IMultipleViewProvider::GetSupportedViews (uiautomationcore.h)
description: Retrieves a collection of control-specific view identifiers. (IMultipleViewProvider.GetSupportedViews)
helpviewer_keywords: ["GetSupportedViews","GetSupportedViews method [Windows Accessibility]","GetSupportedViews method [Windows Accessibility]","IMultipleViewProvider interface","IMultipleViewProvider interface [Windows Accessibility]","GetSupportedViews method","IMultipleViewProvider.GetSupportedViews","IMultipleViewProvider::GetSupportedViews","uiauto.uiauto_IMultipleViewProvider_GetSupportedViews","uiauto_IMultipleViewProvider_GetSupportedViews","uiautomationcore/IMultipleViewProvider::GetSupportedViews","winauto.uiauto_IMultipleViewProvider_GetSupportedViews"]
old-location: winauto\uiauto_IMultipleViewProvider_GetSupportedViews.htm
tech.root: WinAuto
ms.assetid: fd4d5616-c126-455e-84e7-e62e24daf8f9
ms.date: 12/05/2018
ms.keywords: GetSupportedViews, GetSupportedViews method [Windows Accessibility], GetSupportedViews method [Windows Accessibility],IMultipleViewProvider interface, IMultipleViewProvider interface [Windows Accessibility],GetSupportedViews method, IMultipleViewProvider.GetSupportedViews, IMultipleViewProvider::GetSupportedViews, uiauto.uiauto_IMultipleViewProvider_GetSupportedViews, uiauto_IMultipleViewProvider_GetSupportedViews, uiautomationcore/IMultipleViewProvider::GetSupportedViews, winauto.uiauto_IMultipleViewProvider_GetSupportedViews
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
req.dll: Uiautomationcore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMultipleViewProvider::GetSupportedViews
 - uiautomationcore/IMultipleViewProvider::GetSupportedViews
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uiautomationcore.dll
api_name:
 - IMultipleViewProvider.GetSupportedViews
---

# IMultipleViewProvider::GetSupportedViews


## -description

Retrieves a collection of control-specific view identifiers.

## -parameters

### -param pRetVal [out, retval]

Type: <b><a href="/windows/win32/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a>**</b>

Receives a collection of control-specific integer values that identify the views available for a UI Automation element.
				This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

An empty array is returned by UIAutoCore.dll if the provider does not supply any view identifiers.
        

The collection of view identifiers must be identical for all instances of a control.
            

View identifier values can be passed to <a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-imultipleviewprovider-getviewname">IMultipleViewProvider::GetViewName</a>.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-workingwithsafearrays">Best Practices for Using Safe Arrays</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-imultipleviewprovider">IMultipleViewProvider</a>



<b>Reference</b>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>
