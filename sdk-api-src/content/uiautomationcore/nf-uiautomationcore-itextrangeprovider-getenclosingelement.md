---
UID: NF:uiautomationcore.ITextRangeProvider.GetEnclosingElement
title: ITextRangeProvider::GetEnclosingElement (uiautomationcore.h)
description: Returns the innermost element that encloses the text range.
helpviewer_keywords: ["GetEnclosingElement","GetEnclosingElement method [Windows Accessibility]","GetEnclosingElement method [Windows Accessibility]","ITextRangeProvider interface","ITextRangeProvider interface [Windows Accessibility]","GetEnclosingElement method","ITextRangeProvider.GetEnclosingElement","ITextRangeProvider::GetEnclosingElement","uiauto.uiauto_ITextRangeProvider_GetEnclosingElement","uiauto_ITextRangeProvider_GetEnclosingElement","uiautomationcore/ITextRangeProvider::GetEnclosingElement","winauto.uiauto_ITextRangeProvider_GetEnclosingElement"]
old-location: winauto\uiauto_ITextRangeProvider_GetEnclosingElement.htm
tech.root: WinAuto
ms.assetid: 51615c53-3239-41d6-895b-dbda68b6b4db
ms.date: 12/05/2018
ms.keywords: GetEnclosingElement, GetEnclosingElement method [Windows Accessibility], GetEnclosingElement method [Windows Accessibility],ITextRangeProvider interface, ITextRangeProvider interface [Windows Accessibility],GetEnclosingElement method, ITextRangeProvider.GetEnclosingElement, ITextRangeProvider::GetEnclosingElement, uiauto.uiauto_ITextRangeProvider_GetEnclosingElement, uiauto_ITextRangeProvider_GetEnclosingElement, uiautomationcore/ITextRangeProvider::GetEnclosingElement, winauto.uiauto_ITextRangeProvider_GetEnclosingElement
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
 - ITextRangeProvider::GetEnclosingElement
 - uiautomationcore/ITextRangeProvider::GetEnclosingElement
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
 - ITextRangeProvider.GetEnclosingElement
---

# ITextRangeProvider::GetEnclosingElement


## -description

Returns the innermost element that encloses the specified text range.

## -parameters

### -param pRetVal [out, retval]

Type: **[IRawElementProviderSimple](nn-uiautomationcore-irawelementprovidersimple.md)\*\***

The UI Automation provider of the innermost element that encloses the specified [ITextRangeProvider](nn-uiautomationcore-itextrangeprovider.md).

> [!NOTE]
> The enclosing element can span more than just the specified [ITextRangeProvider](nn-uiautomationcore-itextrangeprovider.md).

If no enclosing element is found, the [ITextProvider](nn-uiautomationcore-itextprovider.md) parent of the [ITextRangeProvider](nn-uiautomationcore-itextrangeprovider.md) is returned.

This parameter is passed uninitialized.

## -returns

Type: **[HRESULT](/windows/desktop/WinProg/windows-data-types)**

If this method succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.

## -remarks

### Examples

1. This example shows a text stream that contains an image link. The link is a child of the image, but both span the same text range and are exposed as embedded objects within the text stream.

    *Hello \<Image Link\> World*

    - Both image and link are also descendents of the stream's [ITextProvider](nn-uiautomationcore-itextprovider.md), and either can be specified as the *childElement* in a call to [ITextProvider::RangeFromChild](nf-uiautomationcore-itextprovider-rangefromchild.md).
    - Calling [ITextRangeProvider::RangeFromChild](nf-uiautomationcore-itextprovider-rangefromchild.md), using either the image or the link, returns the same text range (*Range1*).
    - [GetChildren](../uiautomationclient/nf-uiautomationclient-iuiautomationtextrange-getchildren.md) does not return the link.
    - [GetEnclosingElement](nf-uiautomationcore-itextrangeprovider-getenclosingelement.md) does not return the image for any text range.
    - [GetEnclosingElement](nf-uiautomationcore-itextrangeprovider-getenclosingelement.md) on *Range1* returns the link.
    - [GetChildren](../uiautomationclient/nf-uiautomationclient-iuiautomationtextrange-getchildren.md) on *Range1* does not return any children.
    - [GetEnclosingElement](nf-uiautomationcore-itextrangeprovider-getenclosingelement.md) on the text range for the stream's [ITextProvider](nn-uiautomationcore-itextprovider.md) returns the provider.
    - [GetChildren](../uiautomationclient/nf-uiautomationclient-iuiautomationtextrange-getchildren.md) on the text range for the stream's [ITextProvider](nn-uiautomationcore-itextprovider.md) returns only the image.

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
        - [ITextRangeProvider::GetChildren](./nf-uiautomationcore-itextrangeprovider-getchildren.md) returns both table cells.
    - Case 3: Text range that spans the visual content of *Table Cell 1 Table Cell 2*:
        - [ITextRangeProvider::GetEnclosingElement](nf-uiautomationcore-itextrangeprovider-getenclosingelement.md) returns the table element.
        - [ITextRangeProvider::GetChildren](./nf-uiautomationcore-itextrangeprovider-getchildren.md) returns both table cells.
    - Case 4: Text range that spans the word *Cell* of *Table Cell 1*:
        - [ITextRangeProvider::GetEnclosingElement](nf-uiautomationcore-itextrangeprovider-getenclosingelement.md) returns the first cell element.
        - [ITextRangeProvider::GetChildren](./nf-uiautomationcore-itextrangeprovider-getchildren.md) returns no elements.
    - Case 5: A degenerate (empty) text range that represents both starts (table and first cell):
        - [ITextRangeProvider::GetEnclosingElement](nf-uiautomationcore-itextrangeprovider-getenclosingelement.md) returns the first cell element (the innermost element with a range that includes the degenerate range).
        - [ITextRangeProvider::GetChildren](./nf-uiautomationcore-itextrangeprovider-getchildren.md) returns no elements.

## -see-also

[ITextProvider](nn-uiautomationcore-itextprovider.md), [ITextRangeProvider](nn-uiautomationcore-itextrangeprovider.md), [ITextRangeProvider::GetChildren](nf-uiautomationcore-itextrangeprovider-getchildren.md), [UI Automation Providers Overview](/windows/desktop/WinAuto/uiauto-providersoverview)