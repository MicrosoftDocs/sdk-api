---
UID: NF:uiautomationclient.IUIAutomationTextRange.MoveEndpointByRange
title: IUIAutomationTextRange::MoveEndpointByRange (uiautomationclient.h)
description: Moves one endpoint of the current text range to the specified endpoint of a second text range. (IUIAutomationTextRange.MoveEndpointByRange)
helpviewer_keywords: ["IUIAutomationTextRange interface [Windows Accessibility]","MoveEndpointByRange method","IUIAutomationTextRange.MoveEndpointByRange","IUIAutomationTextRange::MoveEndpointByRange","MoveEndpointByRange","MoveEndpointByRange method [Windows Accessibility]","MoveEndpointByRange method [Windows Accessibility]","IUIAutomationTextRange interface","uiauto.uiauto_IUIAutomationTextRange_MoveEndpointByRange","uiauto_IUIAutomationTextRange_MoveEndpointByRange","uiautomationclient/IUIAutomationTextRange::MoveEndpointByRange","winauto.uiauto_IUIAutomationTextRange_MoveEndpointByRange"]
old-location: winauto\uiauto_IUIAutomationTextRange_MoveEndpointByRange.htm
tech.root: WinAuto
ms.assetid: 16cb22ec-2735-41ab-88d5-78a27246af6e
ms.date: 12/05/2018
ms.keywords: IUIAutomationTextRange interface [Windows Accessibility],MoveEndpointByRange method, IUIAutomationTextRange.MoveEndpointByRange, IUIAutomationTextRange::MoveEndpointByRange, MoveEndpointByRange, MoveEndpointByRange method [Windows Accessibility], MoveEndpointByRange method [Windows Accessibility],IUIAutomationTextRange interface, uiauto.uiauto_IUIAutomationTextRange_MoveEndpointByRange, uiauto_IUIAutomationTextRange_MoveEndpointByRange, uiautomationclient/IUIAutomationTextRange::MoveEndpointByRange, winauto.uiauto_IUIAutomationTextRange_MoveEndpointByRange
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationClient.idl
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
 - IUIAutomationTextRange::MoveEndpointByRange
 - uiautomationclient/IUIAutomationTextRange::MoveEndpointByRange
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomationTextRange.MoveEndpointByRange
---

# IUIAutomationTextRange::MoveEndpointByRange


## -description

Moves one endpoint of the current text range to the specified endpoint of a second text range.

## -parameters

### -param srcEndPoint [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint">TextPatternRangeEndpoint</a></b>

An endpoint (either start or end) of the current text range. This is the endpoint to be moved.

### -param range [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextrange">IUIAutomationTextRange</a>*</b>

A second text range from the same text provider as the current text range.

### -param targetEndPoint [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint">TextPatternRangeEndpoint</a></b>

An endpoint (either start or end) of the second text range.   The <i>srcEndPoint</i> of the current text range is moved to this endpoint.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the endpoint being moved crosses the other endpoint of the same text range, that other endpoint is moved also, resulting in a degenerate (empty) range and ensuring the correct ordering of the endpoints (that is, the start is always less than or equal to the end).

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextrange">IUIAutomationTextRange</a>



<a href="/windows/desktop/WinAuto/uiauto-ui-automation-textpattern-overview">UI Automation Support for Textual Content</a>
