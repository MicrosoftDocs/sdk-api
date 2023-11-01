---
UID: NF:uiautomationcore.ITextProvider.RangeFromChild
title: ITextProvider::RangeFromChild (uiautomationcore.h)
description: Retrieves a text range enclosing a child element such as an image, hyperlink, or other embedded object.
helpviewer_keywords: ["ITextProvider interface [Windows Accessibility]","RangeFromChild method","ITextProvider.RangeFromChild","ITextProvider::RangeFromChild","RangeFromChild","RangeFromChild method [Windows Accessibility]","RangeFromChild method [Windows Accessibility]","ITextProvider interface","uiauto.uiauto_ITextProvider_RangeFromChild","uiauto_ITextProvider_RangeFromChild","uiautomationcore/ITextProvider::RangeFromChild","winauto.uiauto_ITextProvider_RangeFromChild"]
old-location: winauto\uiauto_ITextProvider_RangeFromChild.htm
tech.root: WinAuto
ms.assetid: b55ae687-44e1-499f-8341-0bbf960529fd
ms.date: 12/05/2018
ms.keywords: ITextProvider interface [Windows Accessibility],RangeFromChild method, ITextProvider.RangeFromChild, ITextProvider::RangeFromChild, RangeFromChild, RangeFromChild method [Windows Accessibility], RangeFromChild method [Windows Accessibility],ITextProvider interface, uiauto.uiauto_ITextProvider_RangeFromChild, uiauto_ITextProvider_RangeFromChild, uiautomationcore/ITextProvider::RangeFromChild, winauto.uiauto_ITextProvider_RangeFromChild
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
 - ITextProvider::RangeFromChild
 - uiautomationcore/ITextProvider::RangeFromChild
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
 - ITextProvider.RangeFromChild
---

# ITextProvider::RangeFromChild


## -description

Retrieves a text range that encloses the specified child element (for example, an image, hyperlink, or other embedded object).

## -parameters

### -param childElement [in]

Type: **[IRawElementProviderSimple](nn-uiautomationcore-irawelementprovidersimple.md)\***

The UI Automation provider of the specified child element.

### -param pRetVal [out, retval]

Type: **[ITextRangeProvider](nn-uiautomationcore-itextrangeprovider.md)\*\***

The text range that encloses the child element.

This range completely encloses the content of the child element such that:

1. [ITextRangeProvider::GetEnclosingElement](nf-uiautomationcore-itextrangeprovider-getenclosingelement.md) returns the child element itself, or the innermost descendant of the child element that shares the same text range as the child element
2. [ITextRangeProvider::GetChildren](nf-uiautomationcore-itextrangeprovider-getchildren.md) returns children of the element from (1) that are completely enclosed within the range
3. Both endpoints of the range are at the boundaries of the child element

This parameter is passed uninitialized.

## -returns

Type: **[HRESULT](/windows/desktop/WinProg/windows-data-types)**

If this method succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.

> [!NOTE]
> **E_INVALIDARG** is returned if *childElement* is not a descendent of an [ITextProvider](nn-uiautomationcore-itextprovider.md), or is not enclosed by a valid text range.

## -remarks

Each element retrieved with [ITextRangeProvider::GetChildren](nf-uiautomationcore-itextrangeprovider-getchildren.md) also has a valid text range that can be retrieved through [RangeFromChild](nf-uiautomationcore-itextprovider-rangefromchild.md). This includes any elements in the UI Automation tree between the [ITextProvider](nn-uiautomationcore-itextprovider.md) and the child element.

### Examples

1. This example shows a text stream that contains an image link. The link is a child of the image, but both span the same text range and are exposed as embedded objects within the text stream.

    *Hello \<Image Link\> World*

    - Both image and link are also descendents of the stream's [ITextProvider](nn-uiautomationcore-itextprovider.md), and either can be specified as the *childElement* in a call to [ITextProvider::RangeFromChild](nf-uiautomationcore-itextprovider-rangefromchild.md).
    - Calling [ITextRangeProvider::RangeFromChild](nf-uiautomationcore-itextprovider-rangefromchild.md), using either the image or the link, returns the same text range (*Range1*).
    - [ITextRangeProvider::GetChildren](../uiautomationclient/nf-uiautomationclient-iuiautomationtextrange-getchildren.md) does not return the link.
    - [ITextRangeProvider::GetEnclosingElement](nf-uiautomationcore-itextrangeprovider-getenclosingelement.md) does not return the image for any text range.
    - [ITextRangeProvider::GetEnclosingElement](nf-uiautomationcore-itextrangeprovider-getenclosingelement.md) on *Range1* returns the link.
    - [ITextRangeProvider::GetChildren](../uiautomationclient/nf-uiautomationclient-iuiautomationtextrange-getchildren.md) on *Range1* does not return any children.
    - [ITextRangeProvider::GetEnclosingElement](nf-uiautomationcore-itextrangeprovider-getenclosingelement.md) on the text range for the stream's [ITextProvider](nn-uiautomationcore-itextprovider.md) returns the provider.
    - [ITextRangeProvider::GetChildren](../uiautomationclient/nf-uiautomationclient-iuiautomationtextrange-getchildren.md) on the text range for the stream's [ITextProvider](nn-uiautomationcore-itextprovider.md) returns only the image.

2. This example shows a text stream that contains a two-cell table surrounded by text.

    <em>
    <p>Start text</p>
    <p><table><tr><td>Table Cell 1</td><td>Table Cell 2</td></tr></table></p>
    <p>End Text</p>
    </em>

    - Case 1: The stream's [ITextProvider](nn-uiautomationcore-itextprovider.md) and entire text range
        - [ITextRangeProvider::GetEnclosingElement](nf-uiautomationcore-itextrangeprovider-getenclosingelement.md) on the entire text range returns the stream's [ITextProvider](nn-uiautomationcore-itextprovider.md).
        - GetChildren returns all child elements of the stream's [ITextProvider](nn-uiautomationcore-itextprovider.md), only the table element in this case.
    - Case 2: Text range obtained by calling [ITextProvider::RangeFromChild](nf-uiautomationcore-itextprovider-rangefromchild.md) on the table element:
        - [ITextRangeProvider::GetEnclosingElement](nf-uiautomationcore-itextrangeprovider-getenclosingelement.md) returns the table element.
        - [ITextRangeProvider::GetChildren](../uiautomationclient/nf-uiautomationclient-iuiautomationtextrange-getchildren.md) returns both table cells.
    - Case 3: Text range that spans the visual content of *Table Cell 1 Table Cell 2*:
        - [ITextRangeProvider::GetEnclosingElement](nf-uiautomationcore-itextrangeprovider-getenclosingelement.md) returns the table element.
        - [ITextRangeProvider::GetChildren](../uiautomationclient/nf-uiautomationclient-iuiautomationtextrange-getchildren.md) returns both table cells.
    - Case 4: Text range that spans the word *Cell* of *Table Cell 1*:
        - [ITextRangeProvider::GetEnclosingElement](nf-uiautomationcore-itextrangeprovider-getenclosingelement.md) returns the first cell element.
        - [ITextRangeProvider::GetChildren](../uiautomationclient/nf-uiautomationclient-iuiautomationtextrange-getchildren.md) returns no elements.
    - Case 5: A degenerate (empty) text range that represents both starts (table and first cell):
        - [ITextRangeProvider::GetEnclosingElement](nf-uiautomationcore-itextrangeprovider-getenclosingelement.md) returns the first cell element (the innermost element with a range that includes the degenerate range).
        - [ITextRangeProvider::GetChildren](../uiautomationclient/nf-uiautomationclient-iuiautomationtextrange-getchildren.md) returns no elements.

## -see-also

[ITextProvider](nn-uiautomationcore-itextprovider.md), [ITextRangeProvider](nn-uiautomationcore-itextrangeprovider.md), [ITextRangeProvider::GetEnclosingElement](nf-uiautomationcore-itextrangeprovider-getenclosingelement.md), [ITextRangeProvider::GetChildren](nf-uiautomationcore-itextrangeprovider-getchildren.md), [UI Automation Providers Overview](/windows/desktop/WinAuto/uiauto-providersoverview)