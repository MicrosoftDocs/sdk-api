---
UID: NF:uiautomationcore.ISelectionProvider.GetSelection
title: ISelectionProvider::GetSelection (uiautomationcore.h)
description: Retrieves a Microsoft UI Automation provider for each child element that is selected.
helpviewer_keywords: ["GetSelection","GetSelection method [Windows Accessibility]","GetSelection method [Windows Accessibility]","ISelectionProvider interface","ISelectionProvider interface [Windows Accessibility]","GetSelection method","ISelectionProvider.GetSelection","ISelectionProvider::GetSelection","uiauto.uiauto_ISelectionProvider_GetSelection","uiauto_ISelectionProvider_GetSelection","uiautomationcore/ISelectionProvider::GetSelection","winauto.uiauto_ISelectionProvider_GetSelection"]
old-location: winauto\uiauto_ISelectionProvider_GetSelection.htm
tech.root: WinAuto
ms.assetid: f97481b9-f227-47fb-9163-a65a259c9d78
ms.date: 12/05/2018
ms.keywords: GetSelection, GetSelection method [Windows Accessibility], GetSelection method [Windows Accessibility],ISelectionProvider interface, ISelectionProvider interface [Windows Accessibility],GetSelection method, ISelectionProvider.GetSelection, ISelectionProvider::GetSelection, uiauto.uiauto_ISelectionProvider_GetSelection, uiauto_ISelectionProvider_GetSelection, uiautomationcore/ISelectionProvider::GetSelection, winauto.uiauto_ISelectionProvider_GetSelection
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
 - ISelectionProvider::GetSelection
 - uiautomationcore/ISelectionProvider::GetSelection
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
 - ISelectionProvider.GetSelection
---

# ISelectionProvider::GetSelection


## -description

Retrieves a Microsoft UI Automation provider for each child element that is selected.

## -parameters

### -param pRetVal [out, retval]

Type: <b><a href="/windows/win32/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a>**</b>

Receives a pointer to a <a href="/windows/win32/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> that contains an array of pointers to the <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementprovidersimple">IRawElementProviderSimple</a> interfaces
				of the selected elements. This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-workingwithsafearrays">Best Practices for Using Safe Arrays</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iselectionprovider">ISelectionProvider</a>



<b>Reference</b>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>