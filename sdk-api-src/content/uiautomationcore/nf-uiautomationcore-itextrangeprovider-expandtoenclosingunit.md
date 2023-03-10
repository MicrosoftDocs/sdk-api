---
UID: NF:uiautomationcore.ITextRangeProvider.ExpandToEnclosingUnit
title: ITextRangeProvider::ExpandToEnclosingUnit (uiautomationcore.h)
description: Normalizes the text range by the specified text unit. The range is expanded if it is smaller than the specified unit, or shortened if it is longer than the specified unit. (ITextRangeProvider.ExpandToEnclosingUnit)
helpviewer_keywords: ["ExpandToEnclosingUnit","ExpandToEnclosingUnit method [Windows Accessibility]","ExpandToEnclosingUnit method [Windows Accessibility]","ITextRangeProvider interface","ITextRangeProvider interface [Windows Accessibility]","ExpandToEnclosingUnit method","ITextRangeProvider.ExpandToEnclosingUnit","ITextRangeProvider::ExpandToEnclosingUnit","uiauto.uiauto_ITextRangeProvider_ExpandToEnclosingUnit","uiauto_ITextRangeProvider_ExpandToEnclosingUnit","uiautomationcore/ITextRangeProvider::ExpandToEnclosingUnit","winauto.uiauto_ITextRangeProvider_ExpandToEnclosingUnit"]
old-location: winauto\uiauto_ITextRangeProvider_ExpandToEnclosingUnit.htm
tech.root: WinAuto
ms.assetid: 6128b0ef-e78d-4f87-bc70-ab5ac0d055cf
ms.date: 12/05/2018
ms.keywords: ExpandToEnclosingUnit, ExpandToEnclosingUnit method [Windows Accessibility], ExpandToEnclosingUnit method [Windows Accessibility],ITextRangeProvider interface, ITextRangeProvider interface [Windows Accessibility],ExpandToEnclosingUnit method, ITextRangeProvider.ExpandToEnclosingUnit, ITextRangeProvider::ExpandToEnclosingUnit, uiauto.uiauto_ITextRangeProvider_ExpandToEnclosingUnit, uiauto_ITextRangeProvider_ExpandToEnclosingUnit, uiautomationcore/ITextRangeProvider::ExpandToEnclosingUnit, winauto.uiauto_ITextRangeProvider_ExpandToEnclosingUnit
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
 - ITextRangeProvider::ExpandToEnclosingUnit
 - uiautomationcore/ITextRangeProvider::ExpandToEnclosingUnit
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
 - ITextRangeProvider.ExpandToEnclosingUnit
---

# ITextRangeProvider::ExpandToEnclosingUnit


## -description

Normalizes the text range by the specified text unit. The range is expanded if it is smaller than the specified unit, or shortened if it is 
		  longer than the specified unit.

## -parameters

### -param unit [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textunit">TextUnit</a></b>

The type of text units, such as character, word, paragraph, and so on.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Client applications such as screen readers use this method  to retrieve  the full word, sentence, or paragraph that exists at the insertion point or caret position.

Despite its name, the <b>ITextRangeProvider::ExpandToEnclosingUnit</b> method does not necessarily expand a text range. Instead, it "normalizes" a text range by moving the endpoints so that the range encompasses the specified text unit. The range is expanded if it is smaller than the specified unit, or shortened if it is longer than the specified unit. If the range is already an exact quantity of the specified units, it remains unchanged. It is critical that the <b>ExpandToEnclosingUnit</b> method always normalizes text ranges in a consistent manner; otherwise, other aspects of text range manipulation by text unit would be unpredictable. The following diagram shows how <b>ExpandToEnclosingUnit</b> normalizes a text range by moving the endpoints of the range. 
            

<img alt="Diagram showing endpoint positions before and after a call to ExpandToEnclosingUnit" src="./images/ExpandToEnclosingUnit.jpg"/>
<b>ExpandToEnclosingUnit</b> defaults to the next largest text unit 
        supported if the specified text unit is not supported by the control. 
        
        The order, from smallest unit to largest, is as follows:
        

<ul>
<li><i>Character</i></li>
<li><i>Format</i></li>
<li><i>Word</i></li>
<li><i>Line</i></li>
<li><i>Paragraph</i></li>
<li><i>Page</i></li>
<li><i>Document</i></li>
</ul>
<b>ExpandToEnclosingUnit</b> respects both visible and hidden text. 
        

<h3><a id="Range_behavior_when_unit_is_TextUnit__Format"></a><a id="range_behavior_when_unit_is_textunit__format"></a><a id="RANGE_BEHAVIOR_WHEN_UNIT_IS_TEXTUNIT__FORMAT"></a>Range behavior when <i>unit</i> is <code>TextUnit::Format</code></h3>
<code>TextUnit::Format</code> as a <i>unit</i> value positions the boundary of a text range to expand or move the range based on shared text attributes (format) of the text within the range. However, using the format text unit should not move or expand a text range across the boundary of an embedded object, such as an image or hyperlink. For more info, see <a href="/windows/desktop/WinAuto/uiauto-uiautomationtextunits">UI Automation Text Units</a> or <a href="/windows/desktop/WinAuto/uiauto-implementingtextandtextrange">Text and TextRange Control Patterns</a>.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider">ITextProvider</a>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextrangeprovider">ITextRangeProvider</a>



<b>Reference</b>



<a href="/windows/desktop/WinAuto/uiauto-implementingtextandtextrange">Text and TextRange Control Patterns</a>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>
