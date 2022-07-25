---
UID: NF:uiautomationcore.IMultipleViewProvider.SetCurrentView
title: IMultipleViewProvider::SetCurrentView (uiautomationcore.h)
description: Sets the current control-specific view.
helpviewer_keywords: ["IMultipleViewProvider interface [Windows Accessibility]","SetCurrentView method","IMultipleViewProvider.SetCurrentView","IMultipleViewProvider::SetCurrentView","SetCurrentView","SetCurrentView method [Windows Accessibility]","SetCurrentView method [Windows Accessibility]","IMultipleViewProvider interface","uiauto.uiauto_IMultipleViewProvider_SetCurrentView","uiauto_IMultipleViewProvider_SetCurrentView","uiautomationcore/IMultipleViewProvider::SetCurrentView","winauto.uiauto_IMultipleViewProvider_SetCurrentView"]
old-location: winauto\uiauto_IMultipleViewProvider_SetCurrentView.htm
tech.root: WinAuto
ms.assetid: dfa652be-b6b6-44e3-b06a-8ead56f17d2d
ms.date: 12/05/2018
ms.keywords: IMultipleViewProvider interface [Windows Accessibility],SetCurrentView method, IMultipleViewProvider.SetCurrentView, IMultipleViewProvider::SetCurrentView, SetCurrentView, SetCurrentView method [Windows Accessibility], SetCurrentView method [Windows Accessibility],IMultipleViewProvider interface, uiauto.uiauto_IMultipleViewProvider_SetCurrentView, uiauto_IMultipleViewProvider_SetCurrentView, uiautomationcore/IMultipleViewProvider::SetCurrentView, winauto.uiauto_IMultipleViewProvider_SetCurrentView
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
 - IMultipleViewProvider::SetCurrentView
 - uiautomationcore/IMultipleViewProvider::SetCurrentView
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
 - IMultipleViewProvider.SetCurrentView
---

# IMultipleViewProvider::SetCurrentView


## -description

Sets the current control-specific view.

## -parameters

### -param viewId [in]

Type: <b>int</b>

A view identifier.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

View identifiers can be retrieved by using <a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-imultipleviewprovider-getsupportedviews">IMultipleViewProvider::GetSupportedViews</a>.
        

The collection of view identifiers must be identical for all instances of a control.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-imultipleviewprovider">IMultipleViewProvider</a>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>