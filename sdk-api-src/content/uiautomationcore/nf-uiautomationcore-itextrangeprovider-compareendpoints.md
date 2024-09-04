---
UID: NF:uiautomationcore.ITextRangeProvider.CompareEndpoints
title: ITextRangeProvider::CompareEndpoints (uiautomationcore.h)
description: Returns a value that specifies whether two text ranges have identical endpoints.
helpviewer_keywords: ["CompareEndpoints","CompareEndpoints method [Windows Accessibility]","CompareEndpoints method [Windows Accessibility]","ITextRangeProvider interface","ITextRangeProvider interface [Windows Accessibility]","CompareEndpoints method","ITextRangeProvider.CompareEndpoints","ITextRangeProvider::CompareEndpoints","uiauto.uiauto_ITextRangeProvider_CompareEndpoints","uiauto_ITextRangeProvider_CompareEndpoints","uiautomationcore/ITextRangeProvider::CompareEndpoints","winauto.uiauto_ITextRangeProvider_CompareEndpoints"]
old-location: winauto\uiauto_ITextRangeProvider_CompareEndpoints.htm
tech.root: WinAuto
ms.assetid: 88a59d93-f31b-40d5-a8d9-ef114224019b
ms.date: 12/05/2018
ms.keywords: CompareEndpoints, CompareEndpoints method [Windows Accessibility], CompareEndpoints method [Windows Accessibility],ITextRangeProvider interface, ITextRangeProvider interface [Windows Accessibility],CompareEndpoints method, ITextRangeProvider.CompareEndpoints, ITextRangeProvider::CompareEndpoints, uiauto.uiauto_ITextRangeProvider_CompareEndpoints, uiauto_ITextRangeProvider_CompareEndpoints, uiautomationcore/ITextRangeProvider::CompareEndpoints, winauto.uiauto_ITextRangeProvider_CompareEndpoints
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
 - ITextRangeProvider::CompareEndpoints
 - uiautomationcore/ITextRangeProvider::CompareEndpoints
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
 - ITextRangeProvider.CompareEndpoints
---

# ITextRangeProvider::CompareEndpoints


## -description

Returns a value that specifies whether two text ranges have identical endpoints.

## -parameters

### -param endpoint [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint">TextPatternRangeEndpoint</a></b>

The endpoint (starting or ending) of the caller's text range.

### -param targetRange [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextrangeprovider">ITextRangeProvider</a>*</b>

The text range to be compared.

### -param targetEndpoint [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint">TextPatternRangeEndpoint</a></b>

The endpoint (starting or ending) of the target text range.

### -param pRetVal [out, retval]

Type: <b>int*</b>

Receives a value that indicates whether the two text ranges have identical endpoints.
				 This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Returns a negative value if the caller's endpoint occurs earlier in the text than the target endpoint. 


Returns zero if the caller's endpoint is at the same location as the target endpoint. 


Returns a positive value if the caller's endpoint occurs later in the text than the target endpoint.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider">ITextProvider</a>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextrangeprovider">ITextRangeProvider</a>



<b>Reference</b>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>