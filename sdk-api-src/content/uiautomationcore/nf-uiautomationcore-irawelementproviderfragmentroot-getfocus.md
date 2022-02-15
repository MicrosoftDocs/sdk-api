---
UID: NF:uiautomationcore.IRawElementProviderFragmentRoot.GetFocus
title: IRawElementProviderFragmentRoot::GetFocus (uiautomationcore.h)
description: Retrieves the element in this fragment that has the input focus.
helpviewer_keywords: ["GetFocus","GetFocus method [Windows Accessibility]","GetFocus method [Windows Accessibility]","IRawElementProviderFragmentRoot interface","IRawElementProviderFragmentRoot interface [Windows Accessibility]","GetFocus method","IRawElementProviderFragmentRoot.GetFocus","IRawElementProviderFragmentRoot::GetFocus","uiauto.uiauto_IRawElementProviderFragmentRoot_GetFocus","uiauto_IRawElementProviderFragmentRoot_GetFocus","uiautomationcore/IRawElementProviderFragmentRoot::GetFocus","winauto.uiauto_IRawElementProviderFragmentRoot_GetFocus"]
old-location: winauto\uiauto_IRawElementProviderFragmentRoot_GetFocus.htm
tech.root: WinAuto
ms.assetid: 73b5ffc8-1a24-4fa5-8bc4-ae09656a80df
ms.date: 12/05/2018
ms.keywords: GetFocus, GetFocus method [Windows Accessibility], GetFocus method [Windows Accessibility],IRawElementProviderFragmentRoot interface, IRawElementProviderFragmentRoot interface [Windows Accessibility],GetFocus method, IRawElementProviderFragmentRoot.GetFocus, IRawElementProviderFragmentRoot::GetFocus, uiauto.uiauto_IRawElementProviderFragmentRoot_GetFocus, uiauto_IRawElementProviderFragmentRoot_GetFocus, uiautomationcore/IRawElementProviderFragmentRoot::GetFocus, winauto.uiauto_IRawElementProviderFragmentRoot_GetFocus
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
 - IRawElementProviderFragmentRoot::GetFocus
 - uiautomationcore/IRawElementProviderFragmentRoot::GetFocus
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
 - IRawElementProviderFragmentRoot.GetFocus
---

# IRawElementProviderFragmentRoot::GetFocus


## -description

Retrieves the element in this fragment that has the input focus.

## -parameters

### -param pRetVal [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderfragment">IRawElementProviderFragment</a>**</b>

Receives a pointer to the <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderfragment">IRawElementProviderFragment</a> 
                interface of the
				element in this fragment that has the input focus, if any; otherwise <b>NULL</b>. 
				This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderfragmentroot">IRawElementProviderFragmentRoot</a>