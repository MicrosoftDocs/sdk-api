---
UID: NF:uiautomationclient.IUIAutomationTextRange.FindAttribute
title: IUIAutomationTextRange::FindAttribute (uiautomationclient.h)
description: Retrieves a text range subset that has the specified text attribute value.
helpviewer_keywords: ["FindAttribute","FindAttribute method [Windows Accessibility]","FindAttribute method [Windows Accessibility]","IUIAutomationTextRange interface","IUIAutomationTextRange interface [Windows Accessibility]","FindAttribute method","IUIAutomationTextRange.FindAttribute","IUIAutomationTextRange::FindAttribute","uiauto.uiauto_IUIAutomationTextRange_FindAttribute","uiauto_IUIAutomationTextRange_FindAttribute","uiautomationclient/IUIAutomationTextRange::FindAttribute","winauto.uiauto_IUIAutomationTextRange_FindAttribute"]
old-location: winauto\uiauto_IUIAutomationTextRange_FindAttribute.htm
tech.root: WinAuto
ms.assetid: 12722d22-79ca-4390-8155-61234b821256
ms.date: 12/05/2018
ms.keywords: FindAttribute, FindAttribute method [Windows Accessibility], FindAttribute method [Windows Accessibility],IUIAutomationTextRange interface, IUIAutomationTextRange interface [Windows Accessibility],FindAttribute method, IUIAutomationTextRange.FindAttribute, IUIAutomationTextRange::FindAttribute, uiauto.uiauto_IUIAutomationTextRange_FindAttribute, uiauto_IUIAutomationTextRange_FindAttribute, uiautomationclient/IUIAutomationTextRange::FindAttribute, winauto.uiauto_IUIAutomationTextRange_FindAttribute
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
 - IUIAutomationTextRange::FindAttribute
 - uiautomationclient/IUIAutomationTextRange::FindAttribute
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
 - IUIAutomationTextRange.FindAttribute
---

# IUIAutomationTextRange::FindAttribute


## -description

Retrieves a text range subset that has the specified text attribute value.

## -parameters

### -param attr [in]

Type: <b>TEXTATTRIBUTEID</b>

The identifier of the text attribute for the text range subset being retrieved. For a list of text attribute IDs, see <a href="/windows/desktop/WinAuto/uiauto-textattribute-ids">Text Attribute Identifiers</a>.

### -param val [in]

Type: <b><a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a></b>

The value of the attribute. This value must match the type specified for the attribute.

### -param backward [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> if the last occurring text range should be returned instead of the first; otherwise <b>FALSE</b>.

### -param found [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextrange">IUIAutomationTextRange</a>**</b>

Receives a pointer to the text range having a matching attribute and attribute value; otherwise <b>NULL</b>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <b>FindAttribute</b> method retrieves matching text regardless of whether the text is hidden or visible. Use <a href="/windows/desktop/WinAuto/uiauto-textattribute-ids">UIA_IsHiddenAttributeId</a> to check text visibility.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextrange">IUIAutomationTextRange</a>



<a href="/windows/desktop/WinAuto/uiauto-ui-automation-textpattern-overview">UI Automation Support for Textual Content</a>