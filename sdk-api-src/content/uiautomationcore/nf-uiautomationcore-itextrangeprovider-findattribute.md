---
UID: NF:uiautomationcore.ITextRangeProvider.FindAttribute
title: ITextRangeProvider::FindAttribute (uiautomationcore.h)
description: Returns a text range subset that has the specified text attribute value.
helpviewer_keywords: ["FindAttribute","FindAttribute method [Windows Accessibility]","FindAttribute method [Windows Accessibility]","ITextRangeProvider interface","ITextRangeProvider interface [Windows Accessibility]","FindAttribute method","ITextRangeProvider.FindAttribute","ITextRangeProvider::FindAttribute","uiauto.uiauto_ITextRangeProvider_FindAttribute","uiauto_ITextRangeProvider_FindAttribute","uiautomationcore/ITextRangeProvider::FindAttribute","winauto.uiauto_ITextRangeProvider_FindAttribute"]
old-location: winauto\uiauto_ITextRangeProvider_FindAttribute.htm
tech.root: WinAuto
ms.assetid: 623a9b66-7d8c-44d7-b0c1-5ed8a8b8f0c6
ms.date: 12/05/2018
ms.keywords: FindAttribute, FindAttribute method [Windows Accessibility], FindAttribute method [Windows Accessibility],ITextRangeProvider interface, ITextRangeProvider interface [Windows Accessibility],FindAttribute method, ITextRangeProvider.FindAttribute, ITextRangeProvider::FindAttribute, uiauto.uiauto_ITextRangeProvider_FindAttribute, uiauto_ITextRangeProvider_FindAttribute, uiautomationcore/ITextRangeProvider::FindAttribute, winauto.uiauto_ITextRangeProvider_FindAttribute
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
 - ITextRangeProvider::FindAttribute
 - uiautomationcore/ITextRangeProvider::FindAttribute
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
 - ITextRangeProvider.FindAttribute
---

# ITextRangeProvider::FindAttribute


## -description

Returns a text range subset that has the specified text attribute value.

## -parameters

### -param attributeId [in]

Type: <b>TEXTATTRIBUTEID</b>

The identifier of the text attribute. For a list of text attribute IDs, see <a href="/windows/desktop/WinAuto/uiauto-textattribute-ids">Text Attribute Identifiers</a>.

### -param val [in]

Type: <b><a href="/windows/desktop/WinAuto/variant-structure">VARIANT</a></b>

The attribute value to search for. This value must match the type specified for the attribute.

### -param backward [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> if the last occurring text range should be returned instead of the first; otherwise <b>FALSE</b>.

### -param pRetVal [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextrangeprovider">ITextRangeProvider</a>**</b>

Receives a pointer to the text range having a matching attribute and attribute value; otherwise <b>NULL</b>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <b>FindAttribute</b> method retrieves matching text regardless of whether the text is hidden or visible. Clients can use <a href="/windows/desktop/WinAuto/uiauto-textattribute-ids">UIA_IsHiddenAttributeId</a> to check text visibility.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider">ITextProvider</a>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextrangeprovider">ITextRangeProvider</a>



<b>Reference</b>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>