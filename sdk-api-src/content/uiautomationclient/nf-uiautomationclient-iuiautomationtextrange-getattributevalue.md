---
UID: NF:uiautomationclient.IUIAutomationTextRange.GetAttributeValue
title: IUIAutomationTextRange::GetAttributeValue (uiautomationclient.h)
description: Retrieves the value of the specified text attribute across the entire text range.
helpviewer_keywords: ["GetAttributeValue","GetAttributeValue method [Windows Accessibility]","GetAttributeValue method [Windows Accessibility]","IUIAutomationTextRange interface","IUIAutomationTextRange interface [Windows Accessibility]","GetAttributeValue method","IUIAutomationTextRange.GetAttributeValue","IUIAutomationTextRange::GetAttributeValue","uiauto.uiauto_IUIAutomationTextRange_GetAttributeValue","uiauto_IUIAutomationTextRange_GetAttributeValue","uiautomationclient/IUIAutomationTextRange::GetAttributeValue","winauto.uiauto_IUIAutomationTextRange_GetAttributeValue"]
old-location: winauto\uiauto_IUIAutomationTextRange_GetAttributeValue.htm
tech.root: WinAuto
ms.assetid: 7a77774e-7be0-473e-a0c9-e1aa108549e1
ms.date: 12/05/2018
ms.keywords: GetAttributeValue, GetAttributeValue method [Windows Accessibility], GetAttributeValue method [Windows Accessibility],IUIAutomationTextRange interface, IUIAutomationTextRange interface [Windows Accessibility],GetAttributeValue method, IUIAutomationTextRange.GetAttributeValue, IUIAutomationTextRange::GetAttributeValue, uiauto.uiauto_IUIAutomationTextRange_GetAttributeValue, uiauto_IUIAutomationTextRange_GetAttributeValue, uiautomationclient/IUIAutomationTextRange::GetAttributeValue, winauto.uiauto_IUIAutomationTextRange_GetAttributeValue
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
 - IUIAutomationTextRange::GetAttributeValue
 - uiautomationclient/IUIAutomationTextRange::GetAttributeValue
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
 - IUIAutomationTextRange.GetAttributeValue
---

# IUIAutomationTextRange::GetAttributeValue


## -description

Retrieves the value of the specified text attribute across the entire text range.

## -parameters

### -param attr [in]

Type: <b>TEXTATTRIBUTEID</b>

The identifier of the text attribute. For a list of text attribute IDs, see <a href="/windows/desktop/WinAuto/uiauto-textattribute-ids">Text Attribute Identifiers</a>.

### -param value [out, retval]

Type: <b><a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a>*</b>

Receives the value of the specified attribute.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The type of value retrieved by this method depends on the <i>attr</i> parameter. 
For example, calling <b>GetAttributeValue</b> with the <i>attr</i> parameter set to <a href="/windows/desktop/WinAuto/uiauto-textattribute-ids">UIA_FontNameAttributeId</a> returns a string that represents the font name of the text range,  while calling <b>GetAttributeValue</b> with <i>attr</i> set to <a href="/windows/desktop/WinAuto/uiauto-textattribute-ids">UIA_IsItalicAttributeId</a> would return a boolean.





If the attribute specified by <i>attr</i> is not supported, the <i>value</i> parameter receives a value that is equivalent to the  <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-get_reservednotsupportedvalue">IUIAutomation::ReservedNotSupportedValue</a> property. 

A text range can include more than one value for a particular attribute. For example, if a text range includes more than one font, the FontName attribute will have multiple values. An attribute with more than one value is called a  <i>mixed attribute</i>.  You can determine if a particular attribute is    a mixed attribute by comparing the value retrieved from <b>GetAttributeValue</b> with the  <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-get_reservedmixedattributevalue">UIAutomation::ReservedMixedAttributeValue</a> property.

The <b>GetAttributeValue</b> method retrieves the attribute value regardless of whether the text is hidden or visible.
            Use UIA_ IsHiddenAttributeId to check text visibility.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextrange">IUIAutomationTextRange</a>



<a href="/windows/desktop/WinAuto/uiauto-ui-automation-textpattern-overview">UI Automation Support for Textual Content</a>