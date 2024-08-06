---
UID: NF:uiautomationcore.ITextRangeProvider.MoveEndpointByUnit
title: ITextRangeProvider::MoveEndpointByUnit (uiautomationcore.h)
description: Moves one endpoint of the text range the specified number of TextUnit units within the document range.
helpviewer_keywords: ["ITextRangeProvider interface [Windows Accessibility]","MoveEndpointByUnit method","ITextRangeProvider.MoveEndpointByUnit","ITextRangeProvider::MoveEndpointByUnit","MoveEndpointByUnit","MoveEndpointByUnit method [Windows Accessibility]","MoveEndpointByUnit method [Windows Accessibility]","ITextRangeProvider interface","uiauto.uiauto_ITextRangeProvider_MoveEndpointByUnit","uiauto_ITextRangeProvider_MoveEndpointByUnit","uiautomationcore/ITextRangeProvider::MoveEndpointByUnit","winauto.uiauto_ITextRangeProvider_MoveEndpointByUnit"]
old-location: winauto\uiauto_ITextRangeProvider_MoveEndpointByUnit.htm
tech.root: WinAuto
ms.assetid: 3c0b9357-0f51-4044-8a5a-1f68af7a9762
ms.date: 12/05/2018
ms.keywords: ITextRangeProvider interface [Windows Accessibility],MoveEndpointByUnit method, ITextRangeProvider.MoveEndpointByUnit, ITextRangeProvider::MoveEndpointByUnit, MoveEndpointByUnit, MoveEndpointByUnit method [Windows Accessibility], MoveEndpointByUnit method [Windows Accessibility],ITextRangeProvider interface, uiauto.uiauto_ITextRangeProvider_MoveEndpointByUnit, uiauto_ITextRangeProvider_MoveEndpointByUnit, uiautomationcore/ITextRangeProvider::MoveEndpointByUnit, winauto.uiauto_ITextRangeProvider_MoveEndpointByUnit
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
 - ITextRangeProvider::MoveEndpointByUnit
 - uiautomationcore/ITextRangeProvider::MoveEndpointByUnit
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
 - ITextRangeProvider.MoveEndpointByUnit
---

# ITextRangeProvider::MoveEndpointByUnit


## -description

Moves one endpoint of the text range the specified number of <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textunit">TextUnit</a> units within the document range.

## -parameters

### -param endpoint [in]

Type: <b>TextPatternRangeEndpoint</b>

The endpoint to move.

### -param unit [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textunit">TextUnit</a></b>

The type of text units, such as character, word, paragraph, and so on.

### -param count [in]

Type: <b>int</b>

The number of units to move. A positive value moves the endpoint forward. 
                A negative value moves backward. A value of 0 has no effect.

### -param pRetVal [out, retval]

Type: <b>int*</b>

Receives the number of units actually moved, which can be less than the number requested if moving the endpoint runs into the beginning or end of the document.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint">endpoint</a> is moved forward or backward, as specified, to the next available unit boundary. If the original <b>endpoint</b> was at the boundary of the specified text unit, the <b>endpoint</b> is moved to the next available text unit boundary, as shown in the following illustration.

<img alt="Illustration showing endpoints of a text range moving" src="./images/MoveEndpointByUnit.gif"/>
If the <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint">endpoint</a> being moved crosses the other <b>endpoint</b> of the same text range, the other <b>endpoint</b> is also moved, resulting in a degenerate range and ensuring the correct ordering of the <b>endpoint</b> (that is, that the start is always less than or equal to the end).

<b>ITextRangeProvider::MoveEndpointByUnit</b> deprecates up to the next supported text unit if the given text unit is not supported by the control. 
        

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
<code>TextUnit::Format</code> as a <i>unit</i> value positions the boundary of a text range to expand or move the range based on shared text attributes (format) of the text within the range. However, using the format text unit should not move or expand a text range across the boundary of an embedded object, such as an image or hyperlink. For more info, see <a href="/windows/desktop/WinAuto/uiauto-uiautomationtextunits">UI Automation Text Units</a> or <a href="/windows/desktop/WinAuto/uiauto-implementingtextandtextrange">Text and TextRange Control Patterns</a>.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider">ITextProvider</a>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextrangeprovider">ITextRangeProvider</a>



<b>Reference</b>



<a href="/windows/desktop/WinAuto/uiauto-implementingtextandtextrange">Text and TextRange Control Patterns</a>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>