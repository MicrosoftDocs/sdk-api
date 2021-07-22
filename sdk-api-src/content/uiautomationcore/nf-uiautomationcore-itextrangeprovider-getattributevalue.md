---
UID: NF:uiautomationcore.ITextRangeProvider.GetAttributeValue
title: ITextRangeProvider::GetAttributeValue (uiautomationcore.h)
description: Retrieves the value of the specified text attribute across the text range.
helpviewer_keywords: ["GetAttributeValue","GetAttributeValue method [Windows Accessibility]","GetAttributeValue method [Windows Accessibility]","ITextRangeProvider interface","ITextRangeProvider interface [Windows Accessibility]","GetAttributeValue method","ITextRangeProvider.GetAttributeValue","ITextRangeProvider::GetAttributeValue","uiauto.uiauto_ITextRangeProvider_GetAttributeValue","uiauto_ITextRangeProvider_GetAttributeValue","uiautomationcore/ITextRangeProvider::GetAttributeValue","winauto.uiauto_ITextRangeProvider_GetAttributeValue"]
old-location: winauto\uiauto_ITextRangeProvider_GetAttributeValue.htm
tech.root: WinAuto
ms.assetid: a72e780e-30e3-4feb-8f47-46b9f1714061
ms.date: 12/05/2018
ms.keywords: GetAttributeValue, GetAttributeValue method [Windows Accessibility], GetAttributeValue method [Windows Accessibility],ITextRangeProvider interface, ITextRangeProvider interface [Windows Accessibility],GetAttributeValue method, ITextRangeProvider.GetAttributeValue, ITextRangeProvider::GetAttributeValue, uiauto.uiauto_ITextRangeProvider_GetAttributeValue, uiauto_ITextRangeProvider_GetAttributeValue, uiautomationcore/ITextRangeProvider::GetAttributeValue, winauto.uiauto_ITextRangeProvider_GetAttributeValue
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
 - ITextRangeProvider::GetAttributeValue
 - uiautomationcore/ITextRangeProvider::GetAttributeValue
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
 - ITextRangeProvider.GetAttributeValue
---

# ITextRangeProvider::GetAttributeValue


## -description

Retrieves the value of the specified text attribute across the text range.

## -parameters

### -param attributeId [in]

Type: <b>TEXTATTRIBUTEID</b>

The identifier of the text attribute. For a list of text attribute IDs, see <a href="/windows/desktop/WinAuto/uiauto-textattribute-ids">Text Attribute Identifiers</a>.

### -param pRetVal [out, retval]

Type: <b><a href="/windows/desktop/WinAuto/variant-structure">VARIANT</a>*</b>

Receives one of the following. 

<ul>
<li>The address of an object representing the value of the specified attribute. The data type of the value varies depending on the specified attribute. For example, if <i>attributeId</i> is <a href="/windows/desktop/WinAuto/uiauto-textattribute-ids">UIA_FontNameAttributeId</a>,  <b>GetAttributeValue</b> returns a string that represents the font name of the text range,  but if <i>attributeId</i> is <a href="/windows/desktop/WinAuto/uiauto-textattribute-ids">UIA_IsItalicAttributeId</a>,  <b>GetAttributeValue</b> returns a boolean.



</li>
<li>The address of the value retrieved by the <a href="/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiagetreservedmixedattributevalue">UiaGetReservedMixedAttributeValue</a> function, if the value of the specified attribute varies over the text range.</li>
<li>The address of the value retrieved by the <a href="/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiagetreservednotsupportedvalue">UiaGetReservedNotSupportedValue</a> function, if the specified attribute is not supported by the provider or the control. </li>
</ul>
This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <b>GetAttributeValue</b> method should retrieve the attribute value regardless of whether the text is hidden or visible.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider">ITextProvider</a>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextrangeprovider">ITextRangeProvider</a>



<b>Reference</b>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>