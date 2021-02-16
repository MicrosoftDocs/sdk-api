---
UID: NF:uiautomationclient.IUIAutomationTextRange3.GetAttributeValues
title: IUIAutomationTextRange3::GetAttributeValues (uiautomationclient.h)
description: Returns all of the requested text attribute values for a text range in a single cross-process call. This is equivalent to calling GetAttributeValue, except it can retrieve multiple values instead of just one.
helpviewer_keywords: ["GetAttributeValues","GetAttributeValues method [Windows Accessibility]","GetAttributeValues method [Windows Accessibility]","IUIAutomationTextRange3 interface","IUIAutomationTextRange3 interface [Windows Accessibility]","GetAttributeValues method","IUIAutomationTextRange3.GetAttributeValues","IUIAutomationTextRange3::GetAttributeValues","uiautomationclient/IUIAutomationTextRange3::GetAttributeValues","winauto.uiauto_IUIAutomationTextRange3_GetAttributeValues"]
old-location: winauto\uiauto_IUIAutomationTextRange3_GetAttributeValues.htm
tech.root: WinAuto
ms.assetid: 1AF29BF1-A074-4054-B338-7B6922B1415C
ms.date: 12/05/2018
ms.keywords: GetAttributeValues, GetAttributeValues method [Windows Accessibility], GetAttributeValues method [Windows Accessibility],IUIAutomationTextRange3 interface, IUIAutomationTextRange3 interface [Windows Accessibility],GetAttributeValues method, IUIAutomationTextRange3.GetAttributeValues, IUIAutomationTextRange3::GetAttributeValues, uiautomationclient/IUIAutomationTextRange3::GetAttributeValues, winauto.uiauto_IUIAutomationTextRange3_GetAttributeValues
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - IUIAutomationTextRange3::GetAttributeValues
 - uiautomationclient/IUIAutomationTextRange3::GetAttributeValues
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
 - IUIAutomationTextRange3.GetAttributeValues
---

# IUIAutomationTextRange3::GetAttributeValues


## -description

Returns all of the requested text attribute values for a text range in a single cross-process call.  This is equivalent to calling <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue">GetAttributeValue</a>, except it can retrieve multiple values instead of just one.

## -parameters

### -param attributeIds [in]

A list of <a href="/windows/desktop/WinAuto/uiauto-textattribute-ids">text attribute identifiers</a>.

### -param attributeIdCount [in]

The number of <a href="/windows/desktop/WinAuto/uiauto-textattribute-ids">text attribute identifiers</a> in the <i>attributeIds</i> list.

### -param attributeValues [out, retval]

A <b>SAFEARRAY</b> of <b>VARIANT</b> containing values to corresponding text attributes for a text range.

## -returns

Returns <b>S_OK</b> if successful, otherwise an <b>HRESULT</b> error code.

## -remarks

<b>GetAttributeValues</b> only gets the text attributes that are supplied in the call.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextrange3">IUIAutomationTextRange3</a>



<a href="/windows/desktop/WinAuto/uiauto-ui-automation-textpattern-overview">UI Automation Support for Textual Content</a>