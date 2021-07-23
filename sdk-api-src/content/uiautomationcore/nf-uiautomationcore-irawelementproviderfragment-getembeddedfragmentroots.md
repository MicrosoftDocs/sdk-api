---
UID: NF:uiautomationcore.IRawElementProviderFragment.GetEmbeddedFragmentRoots
title: IRawElementProviderFragment::GetEmbeddedFragmentRoots (uiautomationcore.h)
description: Retrieves an array of root fragments that are embedded in the Microsoft UI Automation tree rooted at the current element.
helpviewer_keywords: ["GetEmbeddedFragmentRoots","GetEmbeddedFragmentRoots method [Windows Accessibility]","GetEmbeddedFragmentRoots method [Windows Accessibility]","IRawElementProviderFragment interface","IRawElementProviderFragment interface [Windows Accessibility]","GetEmbeddedFragmentRoots method","IRawElementProviderFragment.GetEmbeddedFragmentRoots","IRawElementProviderFragment::GetEmbeddedFragmentRoots","uiauto.uiauto_IRawElementProviderFragment_GetEmbeddedFragmentRoots","uiauto_IRawElementProviderFragment_GetEmbeddedFragmentRoots","uiautomationcore/IRawElementProviderFragment::GetEmbeddedFragmentRoots","winauto.uiauto_IRawElementProviderFragment_GetEmbeddedFragmentRoots"]
old-location: winauto\uiauto_IRawElementProviderFragment_GetEmbeddedFragmentRoots.htm
tech.root: WinAuto
ms.assetid: 3e64956d-5ab3-46b6-87db-4b0770c8f89a
ms.date: 12/05/2018
ms.keywords: GetEmbeddedFragmentRoots, GetEmbeddedFragmentRoots method [Windows Accessibility], GetEmbeddedFragmentRoots method [Windows Accessibility],IRawElementProviderFragment interface, IRawElementProviderFragment interface [Windows Accessibility],GetEmbeddedFragmentRoots method, IRawElementProviderFragment.GetEmbeddedFragmentRoots, IRawElementProviderFragment::GetEmbeddedFragmentRoots, uiauto.uiauto_IRawElementProviderFragment_GetEmbeddedFragmentRoots, uiauto_IRawElementProviderFragment_GetEmbeddedFragmentRoots, uiautomationcore/IRawElementProviderFragment::GetEmbeddedFragmentRoots, winauto.uiauto_IRawElementProviderFragment_GetEmbeddedFragmentRoots
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
 - IRawElementProviderFragment::GetEmbeddedFragmentRoots
 - uiautomationcore/IRawElementProviderFragment::GetEmbeddedFragmentRoots
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
 - IRawElementProviderFragment.GetEmbeddedFragmentRoots
---

# IRawElementProviderFragment::GetEmbeddedFragmentRoots


## -description

Retrieves an array of root fragments that are embedded in the Microsoft UI Automation tree rooted at the current element.

## -parameters

### -param pRetVal [out, retval]

Type: <b>SAFEARRAY**</b>

Receives an array of pointers to the root fragments, or <b>NULL</b> (see Remarks). This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method returns an array of fragments only if the current element is hosting another automation framework. 
			Most providers return <b>NULL</b>.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-workingwithsafearrays">Best Practices for Using Safe Arrays</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderfragment">IRawElementProviderFragment</a>



<b>Reference</b>