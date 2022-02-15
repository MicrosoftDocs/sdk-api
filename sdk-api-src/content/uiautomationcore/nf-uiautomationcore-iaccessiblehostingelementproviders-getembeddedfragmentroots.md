---
UID: NF:uiautomationcore.IAccessibleHostingElementProviders.GetEmbeddedFragmentRoots
title: IAccessibleHostingElementProviders::GetEmbeddedFragmentRoots (uiautomationcore.h)
description: Retrieves the Microsoft Active Accessibility providers of all windowless Microsoft ActiveX controls that have a Microsoft UI Automation provider implementation, and are hosted in a Microsoft Active Accessibility object that implements the IAccessibleHostingElementProviders interface.
helpviewer_keywords: ["GetEmbeddedFragmentRoots","GetEmbeddedFragmentRoots method [Windows Accessibility]","GetEmbeddedFragmentRoots method [Windows Accessibility]","IAccessibleHostingElementProviders interface","IAccessibleHostingElementProviders interface [Windows Accessibility]","GetEmbeddedFragmentRoots method","IAccessibleHostingElementProviders.GetEmbeddedFragmentRoots","IAccessibleHostingElementProviders::GetEmbeddedFragmentRoots","uiautomationcore/IAccessibleHostingElementProviders::GetEmbeddedFragmentRoots","winauto.uiauto_IAccessibleHostingElementProviders_GetEmbeddedFragmentRoots"]
old-location: winauto\uiauto_IAccessibleHostingElementProviders_GetEmbeddedFragmentRoots.htm
tech.root: WinAuto
ms.assetid: 39A9665F-C2F3-48A2-A165-50AD3B82455F
ms.date: 12/05/2018
ms.keywords: GetEmbeddedFragmentRoots, GetEmbeddedFragmentRoots method [Windows Accessibility], GetEmbeddedFragmentRoots method [Windows Accessibility],IAccessibleHostingElementProviders interface, IAccessibleHostingElementProviders interface [Windows Accessibility],GetEmbeddedFragmentRoots method, IAccessibleHostingElementProviders.GetEmbeddedFragmentRoots, IAccessibleHostingElementProviders::GetEmbeddedFragmentRoots, uiautomationcore/IAccessibleHostingElementProviders::GetEmbeddedFragmentRoots, winauto.uiauto_IAccessibleHostingElementProviders_GetEmbeddedFragmentRoots
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - IAccessibleHostingElementProviders::GetEmbeddedFragmentRoots
 - uiautomationcore/IAccessibleHostingElementProviders::GetEmbeddedFragmentRoots
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
 - IAccessibleHostingElementProviders.GetEmbeddedFragmentRoots
---

# IAccessibleHostingElementProviders::GetEmbeddedFragmentRoots


## -description

Retrieves the  Microsoft Active Accessibility providers of  all windowless Microsoft ActiveX controls that have a Microsoft UI Automation provider implementation, and are hosted in a Microsoft Active Accessibility object that implements the <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iaccessiblehostingelementproviders">IAccessibleHostingElementProviders</a> interface.

## -parameters

### -param pRetVal [out, retval]

Type: <b>SAFEARRAY**</b>

Receives the <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderfragmentroot">IRawElementProviderFragmentRoot</a> interface pointers.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The container of windowless ActiveX controls implements this method on the same object that implements the <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> interface.  When called, this method queries each of the contained windowless ActiveX controls for an <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderfragmentroot">IRawElementProviderFragmentRoot</a> pointer, and then adds the pointer to the safe array.  

This method should not include any providers that do not implement <b>IRawElementProviderFragmentRoot</b>.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iaccessiblehostingelementproviders">IAccessibleHostingElementProviders</a>