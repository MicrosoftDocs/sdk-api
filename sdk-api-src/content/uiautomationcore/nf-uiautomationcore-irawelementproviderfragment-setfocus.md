---
UID: NF:uiautomationcore.IRawElementProviderFragment.SetFocus
title: IRawElementProviderFragment::SetFocus (uiautomationcore.h)
description: Sets the focus to this element.
helpviewer_keywords: ["IRawElementProviderFragment interface [Windows Accessibility]","SetFocus method","IRawElementProviderFragment.SetFocus","IRawElementProviderFragment::SetFocus","SetFocus","SetFocus method [Windows Accessibility]","SetFocus method [Windows Accessibility]","IRawElementProviderFragment interface","uiauto.uiauto_IRawElementProviderFragment_SetFocus","uiauto_IRawElementProviderFragment_SetFocus","uiautomationcore/IRawElementProviderFragment::SetFocus","winauto.uiauto_IRawElementProviderFragment_SetFocus"]
old-location: winauto\uiauto_IRawElementProviderFragment_SetFocus.htm
tech.root: WinAuto
ms.assetid: 343959bc-42d0-4289-b507-7da78cee28f2
ms.date: 12/05/2018
ms.keywords: IRawElementProviderFragment interface [Windows Accessibility],SetFocus method, IRawElementProviderFragment.SetFocus, IRawElementProviderFragment::SetFocus, SetFocus, SetFocus method [Windows Accessibility], SetFocus method [Windows Accessibility],IRawElementProviderFragment interface, uiauto.uiauto_IRawElementProviderFragment_SetFocus, uiauto_IRawElementProviderFragment_SetFocus, uiautomationcore/IRawElementProviderFragment::SetFocus, winauto.uiauto_IRawElementProviderFragment_SetFocus
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
 - IRawElementProviderFragment::SetFocus
 - uiautomationcore/IRawElementProviderFragment::SetFocus
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
 - IRawElementProviderFragment.SetFocus
---

# IRawElementProviderFragment::SetFocus


## -description

Sets the focus to this element.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The Microsoft UI Automation framework will ensure that the part of the interface that hosts this fragment is 
			already focused before calling this method. Your implementation should update only its internal focus state; 
			for example, by repainting a list item to show that it has the focus. If you prefer that UI Automation 
			not focus the parent window, set <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-provideroptions">ProviderOptions_ProviderOwnsSetFocus</a> in <a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementprovidersimple-get_provideroptions">IRawElementProviderSimple::ProviderOptions</a> for the fragment root.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderfragment">IRawElementProviderFragment</a>
