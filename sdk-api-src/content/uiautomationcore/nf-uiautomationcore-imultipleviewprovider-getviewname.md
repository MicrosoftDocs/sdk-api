---
UID: NF:uiautomationcore.IMultipleViewProvider.GetViewName
title: IMultipleViewProvider::GetViewName (uiautomationcore.h)
description: Retrieves the name of a control-specific view. (IMultipleViewProvider.GetViewName)
helpviewer_keywords: ["GetViewName","GetViewName method [Windows Accessibility]","GetViewName method [Windows Accessibility]","IMultipleViewProvider interface","IMultipleViewProvider interface [Windows Accessibility]","GetViewName method","IMultipleViewProvider.GetViewName","IMultipleViewProvider::GetViewName","uiauto.uiauto_IMultipleViewProvider_GetViewName","uiauto_IMultipleViewProvider_GetViewName","uiautomationcore/IMultipleViewProvider::GetViewName","winauto.uiauto_IMultipleViewProvider_GetViewName"]
old-location: winauto\uiauto_IMultipleViewProvider_GetViewName.htm
tech.root: WinAuto
ms.assetid: 72e9bca3-22cd-4f5b-9481-289bdfaf58e8
ms.date: 12/05/2018
ms.keywords: GetViewName, GetViewName method [Windows Accessibility], GetViewName method [Windows Accessibility],IMultipleViewProvider interface, IMultipleViewProvider interface [Windows Accessibility],GetViewName method, IMultipleViewProvider.GetViewName, IMultipleViewProvider::GetViewName, uiauto.uiauto_IMultipleViewProvider_GetViewName, uiauto_IMultipleViewProvider_GetViewName, uiautomationcore/IMultipleViewProvider::GetViewName, winauto.uiauto_IMultipleViewProvider_GetViewName
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
 - IMultipleViewProvider::GetViewName
 - uiautomationcore/IMultipleViewProvider::GetViewName
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
 - IMultipleViewProvider.GetViewName
---

# IMultipleViewProvider::GetViewName


## -description

Retrieves the name of a control-specific view.

## -parameters

### -param viewId [in]

Type: <b>int</b>

A view identifier.

### -param pRetVal [out, retval]

Type: <b>BSTR*</b>

Receives a localized name for the view. 
                This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

View identifiers can be retrieved by using <a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-imultipleviewprovider-getsupportedviews">IMultipleViewProvider::GetSupportedViews</a>.
            

The collection of view identifiers must be identical for all instances of a control.
            

View names must be suitable for use in text-to-speech, Braille, and other accessible applications.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-imultipleviewprovider">IMultipleViewProvider</a>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>
