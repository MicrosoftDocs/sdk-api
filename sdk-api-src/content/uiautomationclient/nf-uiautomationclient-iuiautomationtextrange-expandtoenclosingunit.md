---
UID: NF:uiautomationclient.IUIAutomationTextRange.ExpandToEnclosingUnit
title: IUIAutomationTextRange::ExpandToEnclosingUnit (uiautomationclient.h)
description: Normalizes the text range by the specified text unit. The range is expanded if it is smaller than the specified unit, or shortened if it is longer than the specified unit.
old-location: winauto\uiauto_IUIAutomationTextRange_ExpandToEnclosingUnit.htm
tech.root: WinAuto
ms.assetid: 09ec62c1-f738-43af-bd6c-b45fdfb32236
ms.date: 12/05/2018
ms.keywords: ExpandToEnclosingUnit, ExpandToEnclosingUnit method [Windows Accessibility], ExpandToEnclosingUnit method [Windows Accessibility],IUIAutomationTextRange interface, IUIAutomationTextRange interface [Windows Accessibility],ExpandToEnclosingUnit method, IUIAutomationTextRange.ExpandToEnclosingUnit, IUIAutomationTextRange::ExpandToEnclosingUnit, uiauto.uiauto_IUIAutomationTextRange_ExpandToEnclosingUnit, uiauto_IUIAutomationTextRange_ExpandToEnclosingUnit, uiautomationclient/IUIAutomationTextRange::ExpandToEnclosingUnit, winauto.uiauto_IUIAutomationTextRange_ExpandToEnclosingUnit
ms.topic: method
f1_keywords:
- uiautomationclient/IUIAutomationTextRange.ExpandToEnclosingUnit
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- UIAutomationClient.h
api_name:
- IUIAutomationTextRange.ExpandToEnclosingUnit
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomationTextRange::ExpandToEnclosingUnit

## -description

Normalizes the text range by the specified text unit. The range is expanded if it is smaller than the specified unit, or shortened if it is longer than the specified unit.

## -parameters

#### - textUnit [in]

<<<<<<< HEAD
Type: **[TextUnit](../uiautomationcore/ne-uiautomationcore-textunit.md)**
=======
Type: **[TextUnit enumeration](../uiautomationcore/ne-uiautomationcore-textunit.md)**
>>>>>>> master

The text unit, such as line or paragraph.

## -returns

Type: **[HRESULT](https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types)**

If this method succeeds, it returns S_OK. Otherwise, it returns an HRESULT error code.

## -remarks

<<<<<<< HEAD
> ### Parameters
>
> `textUnit` [in]
>
> Type: **[TextUnit](../uiautomationcore/ne-uiautomationcore-textunit.md)**
>
> The text unit, such as line or paragraph.

=======
>>>>>>> master
Client applications such as screen readers use this method  to retrieve  the full word, sentence, or paragraph that exists at the insertion point or caret position.

Despite its name, the ExpandToEnclosingUnit method does not necessarily expand a text range. Instead, it "normalizes" a text range by moving the endpoints so that the range encompasses the specified text unit. The range is expanded if it is smaller than the specified unit, or shortened if it is longer than the specified unit. If the range is already an exact quantity of the specified units, it remains unchanged. The following diagram shows how ExpandToEnclosingUnit normalizes a text range by moving the endpoints of the range.

![Diagram showing endpoints before and after ExpandToEnclosingUnit](./images/ExpandToEnclosingUnit.jpg)

*Diagram showing endpoints before and after ExpandToEnclosingUnit*

ExpandToEnclosingUnit defaults to the next largest text unit supported if the specified text unit is not supported by the control.

The order, from smallest unit to largest, is as follows:

- Character
- Format
- Word
- Line
- Paragraph
- Page
- Document

ExpandToEnclosingUnit respects both visible and hidden text.

### Range behavior when *unit* is `TextUnit::Format`

`TextUnit::Format`, as a *unit* value, positions the boundary of a text range to expand or move the range based on shared text attributes (format) of the text within the range. However, using the Format text unit does not move or expand a text range across the boundary of an embedded object, such as an image or hyperlink. For more info, see [UI Automation Text Units](https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-uiautomationtextunits) or [UI Automation Support for Textual Content](https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-ui-automation-textpattern-overview).

## -see-also

<b>Conceptual</b>

[IUIAutomationTextRange interface](nn-uiautomationclient-iuiautomationtextrange.md)

<b>Reference</b>

[UI Automation Support for Textual Content](https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-ui-automation-textpattern-overview)
