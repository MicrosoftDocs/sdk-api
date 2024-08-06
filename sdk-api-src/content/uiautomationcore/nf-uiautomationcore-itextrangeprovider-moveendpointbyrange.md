---
UID: NF:uiautomationcore.ITextRangeProvider.MoveEndpointByRange
title: ITextRangeProvider::MoveEndpointByRange (uiautomationcore.h)
description: Moves one endpoint of the current text range to the specified endpoint of a second text range. (ITextRangeProvider.MoveEndpointByRange)
helpviewer_keywords: ["ITextRangeProvider interface [Windows Accessibility]","MoveEndpointByRange method","ITextRangeProvider.MoveEndpointByRange","ITextRangeProvider::MoveEndpointByRange","MoveEndpointByRange","MoveEndpointByRange method [Windows Accessibility]","MoveEndpointByRange method [Windows Accessibility]","ITextRangeProvider interface","uiauto.uiauto_ITextRangeProvider_MoveEndpointByRange","uiauto_ITextRangeProvider_MoveEndpointByRange","uiautomationcore/ITextRangeProvider::MoveEndpointByRange","winauto.uiauto_ITextRangeProvider_MoveEndpointByRange"]
old-location: winauto\uiauto_ITextRangeProvider_MoveEndpointByRange.htm
tech.root: WinAuto
ms.assetid: 86411603-c37f-4192-95d1-8ac9b6ab6c44
ms.date: 12/05/2018
ms.keywords: ITextRangeProvider interface [Windows Accessibility],MoveEndpointByRange method, ITextRangeProvider.MoveEndpointByRange, ITextRangeProvider::MoveEndpointByRange, MoveEndpointByRange, MoveEndpointByRange method [Windows Accessibility], MoveEndpointByRange method [Windows Accessibility],ITextRangeProvider interface, uiauto.uiauto_ITextRangeProvider_MoveEndpointByRange, uiauto_ITextRangeProvider_MoveEndpointByRange, uiautomationcore/ITextRangeProvider::MoveEndpointByRange, winauto.uiauto_ITextRangeProvider_MoveEndpointByRange
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
 - ITextRangeProvider::MoveEndpointByRange
 - uiautomationcore/ITextRangeProvider::MoveEndpointByRange
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
 - ITextRangeProvider.MoveEndpointByRange
---

# ITextRangeProvider::MoveEndpointByRange


## -description

Moves one endpoint of the current text range to the specified endpoint of a second text range.

## -parameters

### -param endpoint [in]

Type: <b>TextPatternRangeEndpoint</b>

An endpoint (either start or end) of the current text range. This is the endpoint to be moved.

### -param targetRange [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextrangeprovider">ITextRangeProvider</a>*</b>

A second text range from the same text provider as the current text range.

### -param targetEndpoint [in]

Type: <b>TextPatternRangeEndpoint</b>

An endpoint (either start or end) of the second text range.   The <i>endpoint</i> of the current text range is moved to this endpoint.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the endpoint being moved crosses the other endpoint of the same text range, that other endpoint is moved also, resulting in a degenerate (empty) range and ensuring the correct ordering of the endpoints (that is, the start is always less than or equal to the end).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider">ITextProvider</a>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextrangeprovider">ITextRangeProvider</a>



<b>Reference</b>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>
