---
UID: NF:uiautomationcore.IRawElementProviderSimple.GetPatternProvider
title: IRawElementProviderSimple::GetPatternProvider (uiautomationcore.h)
description: Retrieves a pointer to an object that provides support for a control pattern on a Microsoft UI Automation element.
helpviewer_keywords: ["GetPatternProvider","GetPatternProvider method [Windows Accessibility]","GetPatternProvider method [Windows Accessibility]","IRawElementProviderSimple interface","IRawElementProviderSimple interface [Windows Accessibility]","GetPatternProvider method","IRawElementProviderSimple.GetPatternProvider","IRawElementProviderSimple::GetPatternProvider","uiauto.uiauto_IRawElementProviderSimple_GetPatternProvider","uiauto_IRawElementProviderSimple_GetPatternProvider","uiautomationcore/IRawElementProviderSimple::GetPatternProvider","winauto.uiauto_IRawElementProviderSimple_GetPatternProvider"]
old-location: winauto\uiauto_IRawElementProviderSimple_GetPatternProvider.htm
tech.root: WinAuto
ms.assetid: 8315c1d4-6347-462f-9c96-121f216faf88
ms.date: 12/05/2018
ms.keywords: GetPatternProvider, GetPatternProvider method [Windows Accessibility], GetPatternProvider method [Windows Accessibility],IRawElementProviderSimple interface, IRawElementProviderSimple interface [Windows Accessibility],GetPatternProvider method, IRawElementProviderSimple.GetPatternProvider, IRawElementProviderSimple::GetPatternProvider, uiauto.uiauto_IRawElementProviderSimple_GetPatternProvider, uiauto_IRawElementProviderSimple_GetPatternProvider, uiautomationcore/IRawElementProviderSimple::GetPatternProvider, winauto.uiauto_IRawElementProviderSimple_GetPatternProvider
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
 - IRawElementProviderSimple::GetPatternProvider
 - uiautomationcore/IRawElementProviderSimple::GetPatternProvider
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
 - IRawElementProviderSimple.GetPatternProvider
---

# IRawElementProviderSimple::GetPatternProvider


## -description

Retrieves a pointer to an object that provides support for a control pattern on a Microsoft UI Automation element.

## -parameters

### -param patternId [in]

Type: <b>PATTERNID</b>

The identifier of the control pattern. For a list of control pattern IDs, see <a href="/windows/desktop/WinAuto/uiauto-controlpattern-ids">Control Pattern Identifiers</a>.

### -param pRetVal [out, retval]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>**</b>

Receives a pointer to the object that supports the control pattern,
				or <b>NULL</b> if the control pattern is not supported. 
				This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementprovidersimple">IRawElementProviderSimple</a>