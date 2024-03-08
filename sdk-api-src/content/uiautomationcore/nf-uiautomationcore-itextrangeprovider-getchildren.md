---
UID: NF:uiautomationcore.ITextRangeProvider.GetChildren
title: ITextRangeProvider::GetChildren (uiautomationcore.h)
description: Retrieves a collection of all embedded objects that fall within the text range. (ITextRangeProvider.GetChildren)
helpviewer_keywords: ["GetChildren","GetChildren method [Windows Accessibility]","GetChildren method [Windows Accessibility]","ITextRangeProvider interface","ITextRangeProvider interface [Windows Accessibility]","GetChildren method","ITextRangeProvider.GetChildren","ITextRangeProvider::GetChildren","uiauto.uiauto_ITextRangeProvider_GetChildren","uiauto_ITextRangeProvider_GetChildren","uiautomationcore/ITextRangeProvider::GetChildren","winauto.uiauto_ITextRangeProvider_GetChildren"]
old-location: winauto\uiauto_ITextRangeProvider_GetChildren.htm
tech.root: WinAuto
ms.assetid: 2b68a7eb-8ff5-4e8c-830b-e180b2c08be4
ms.date: 12/05/2018
ms.keywords: GetChildren, GetChildren method [Windows Accessibility], GetChildren method [Windows Accessibility],ITextRangeProvider interface, ITextRangeProvider interface [Windows Accessibility],GetChildren method, ITextRangeProvider.GetChildren, ITextRangeProvider::GetChildren, uiauto.uiauto_ITextRangeProvider_GetChildren, uiauto_ITextRangeProvider_GetChildren, uiautomationcore/ITextRangeProvider::GetChildren, winauto.uiauto_ITextRangeProvider_GetChildren
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
 - ITextRangeProvider::GetChildren
 - uiautomationcore/ITextRangeProvider::GetChildren
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
 - ITextRangeProvider.GetChildren
---

# ITextRangeProvider::GetChildren


## -description

Retrieves a collection of all elements that are both contained (either partially or completely) within the specified text range, and are child elements of the [enclosing element](nf-uiautomationcore-itextrangeprovider-getenclosingelement.md) for the specified text range.

## -parameters

### -param pRetVal [out, retval]

Type: **[SAFEARRAY](../oaidl/ns-oaidl-safearray.md)\*\***

An array of pointers to the <a href="/windows/win32/api/uiautomationcore/nn-uiautomationcore-irawelementprovidersimple">IRawElementProviderSimple</a> interfaces for all child elements that are enclosed by the text range (sorted by the Start endpoint of their ranges).

If the text range does not include any child elements, an empty collection is returned.

This parameter is passed uninitialized.

## -returns

Type: **[HRESULT](/windows/desktop/WinProg/windows-data-types)**

If this method succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.

## -remarks

Each element retrieved with [ITextRangeProvider::GetChildren]() has a valid text range that can be retrieved through [RangeFromChild](nf-uiautomationcore-itextprovider-rangefromchild.md). This includes any elements in the UI Automation tree between the [ITextProvider](nn-uiautomationcore-itextprovider.md) and the child element.

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
        - [ITextRangeProvider::GetChildren]()
 returns both table cells.
    - Case 3: Text range that spans the visual content of *Table Cell 1 Table Cell 2*:
        - [ITextRangeProvider::GetEnclosingElement](nf-uiautomationcore-itextrangeprovider-getenclosingelement.md) returns the table element.
        - [ITextRangeProvider::GetChildren]()
 returns both table cells.
    - Case 4: Text range that spans the word *Cell* of *Table Cell 1*:
        - [ITextRangeProvider::GetEnclosingElement](nf-uiautomationcore-itextrangeprovider-getenclosingelement.md) returns the first cell element.
        - [ITextRangeProvider::GetChildren]()
 returns no elements.
    - Case 5: A degenerate (empty) text range that represents both starts (table and first cell):
        - [ITextRangeProvider::GetEnclosingElement](nf-uiautomationcore-itextrangeprovider-getenclosingelement.md) returns the first cell element (the innermost element with a range that includes the degenerate range).
        - [ITextRangeProvider::GetChildren]()
 returns no elements.

## -see-also

[ITextProvider](nn-uiautomationcore-itextprovider.md), [ITextRangeProvider](nn-uiautomationcore-itextrangeprovider.md), [GetEnclosingElement](nf-uiautomationcore-itextrangeprovider-getenclosingelement.md), [ITextProvider::RangeFromChild](nf-uiautomationcore-itextprovider-rangefromchild.md), [UI Automation Providers Overview](/windows/desktop/WinAuto/uiauto-providersoverview), [Best Practices for Using Safe Arrays](/windows/desktop/WinAuto/uiauto-workingwithsafearrays)
