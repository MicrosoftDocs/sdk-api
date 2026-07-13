---
UID: NF:uiautomationclient.IUIAutomationTextRange.MoveEndpointByUnit
title: IUIAutomationTextRange::MoveEndpointByUnit (uiautomationclient.h)
description: Moves one endpoint of the text range the specified number of text units within the document range.
helpviewer_keywords: ["IUIAutomationTextRange interface [Windows Accessibility]","MoveEndpointByUnit method","IUIAutomationTextRange.MoveEndpointByUnit","IUIAutomationTextRange::MoveEndpointByUnit","MoveEndpointByUnit","MoveEndpointByUnit method [Windows Accessibility]","MoveEndpointByUnit method [Windows Accessibility]","IUIAutomationTextRange interface","uiauto.uiauto_IUIAutomationTextRange_MoveEndpointByUnit","uiauto_IUIAutomationTextRange_MoveEndpointByUnit","uiautomationclient/IUIAutomationTextRange::MoveEndpointByUnit","winauto.uiauto_IUIAutomationTextRange_MoveEndpointByUnit"]
old-location: winauto\uiauto_IUIAutomationTextRange_MoveEndpointByUnit.htm
tech.root: WinAuto
ms.assetid: 8724db1f-b8ed-4e00-9661-c22dd412653c
ms.date: 12/05/2018
ms.keywords: IUIAutomationTextRange interface [Windows Accessibility],MoveEndpointByUnit method, IUIAutomationTextRange.MoveEndpointByUnit, IUIAutomationTextRange::MoveEndpointByUnit, MoveEndpointByUnit, MoveEndpointByUnit method [Windows Accessibility], MoveEndpointByUnit method [Windows Accessibility],IUIAutomationTextRange interface, uiauto.uiauto_IUIAutomationTextRange_MoveEndpointByUnit, uiauto_IUIAutomationTextRange_MoveEndpointByUnit, uiautomationclient/IUIAutomationTextRange::MoveEndpointByUnit, winauto.uiauto_IUIAutomationTextRange_MoveEndpointByUnit
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
 - IUIAutomationTextRange::MoveEndpointByUnit
 - uiautomationclient/IUIAutomationTextRange::MoveEndpointByUnit
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
 - IUIAutomationTextRange.MoveEndpointByUnit
---

# IUIAutomationTextRange::MoveEndpointByUnit


## -description

Moves one endpoint of the text range the specified number of text units within the document range.

## -parameters

### -param endpoint [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint">TextPatternRangeEndpoint</a></b>

A value specifying the endpoint (start or end) to move.

### -param unit [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textunit">TextUnit</a></b>

A value specifying the textual unit for moving, such as line or paragraph.

### -param count [in]

Type: <b>int</b>

The number of units to move. A positive count moves the endpoint forward. A negative count moves backward. A count of 0 has no effect.

### -param moved [out, retval]

Type: <b>int*</b>

Receives the count of units actually moved. This value can be less than the number requested if moving the endpoint runs into the beginning or end of the document.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint">endpoint</a> is moved forward or backward, as specified, to the next available unit boundary. If the original <b>endpoint</b> was at the boundary of the specified text unit, the <b>endpoint</b> is moved to the next available text unit boundary, as shown in the following illustration.

<img alt="Illustration showing endpoints of a text range moving" src="./images/moveendpointbyunit.gif"/>
If the <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint">endpoint</a> being moved crosses the other <b>endpoint</b> of the same text range, the other <b>endpoint</b> is also moved, resulting in a degenerate range and ensuring the correct ordering of the <b>endpoint</b> (that is, that the start is always less than or equal to the end).


<a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextrangeprovider-moveendpointbyunit">MoveEndpointByUnit</a> deprecates up to the next supported text unit if the given text unit is not supported by the control. 
        

The order, from smallest unit to largest, is listed here.
        

<ul>
<li><i>Character</i></li>
<li><i>Format</i></li>
<li><i>Word</i></li>
<li><i>Line</i></li>
<li><i>Paragraph</i></li>
<li><i>Page</i></li>
<li><i>Document</i></li>
</ul>
<h3><a id="Range_behavior_when_unit_is_TextUnit__Format"></a><a id="range_behavior_when_unit_is_textunit__format"></a><a id="RANGE_BEHAVIOR_WHEN_UNIT_IS_TEXTUNIT__FORMAT"></a>Range behavior when <i>unit</i> is <code>TextUnit::Format</code></h3>
<code>TextUnit::Format</code> as a <i>unit</i> value positions the boundary of a text range to expand or move the range based on shared text attributes (format) of the text within the range. However, using the format text unit will not move or expand a text range across the boundary of an embedded object, such as an image or hyperlink. For more info, see <a href="/windows/desktop/WinAuto/uiauto-uiautomationtextunits">UI Automation Text Units</a> or <a href="/windows/desktop/WinAuto/uiauto-ui-automation-textpattern-overview">UI Automation Support for Textual Content</a>.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextrange">IUIAutomationTextRange</a>



<a href="/windows/desktop/WinAuto/uiauto-ui-automation-textpattern-overview">UI Automation Support for Textual Content</a>