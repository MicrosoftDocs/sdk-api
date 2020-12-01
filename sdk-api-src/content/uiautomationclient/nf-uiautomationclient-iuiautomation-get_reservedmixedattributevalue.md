---
UID: NF:uiautomationclient.IUIAutomation.get_ReservedMixedAttributeValue
title: IUIAutomation::get_ReservedMixedAttributeValue (uiautomationclient.h)
description: Retrieves a static token object representing a text attribute that is a mixed attribute.
helpviewer_keywords: ["IUIAutomation interface [Windows Accessibility]","ReservedMixedAttributeValue property","IUIAutomation.ReservedMixedAttributeValue","IUIAutomation.get_ReservedMixedAttributeValue","IUIAutomation::ReservedMixedAttributeValue","IUIAutomation::get_ReservedMixedAttributeValue","ReservedMixedAttributeValue property [Windows Accessibility]","ReservedMixedAttributeValue property [Windows Accessibility]","IUIAutomation interface","get_ReservedMixedAttributeValue","uiauto.uiauto_IUIAutomation_ReservedMixedAttributeValue","uiauto_IUIAutomation_ReservedMixedAttributeValue","uiautomationclient/IUIAutomation::ReservedMixedAttributeValue","uiautomationclient/IUIAutomation::get_ReservedMixedAttributeValue","winauto.uiauto_IUIAutomation_ReservedMixedAttributeValue"]
old-location: winauto\uiauto_IUIAutomation_ReservedMixedAttributeValue.htm
tech.root: WinAuto
ms.assetid: 5b225507-deee-4f2c-a17b-f0e96963a1d0
ms.date: 12/05/2018
ms.keywords: IUIAutomation interface [Windows Accessibility],ReservedMixedAttributeValue property, IUIAutomation.ReservedMixedAttributeValue, IUIAutomation.get_ReservedMixedAttributeValue, IUIAutomation::ReservedMixedAttributeValue, IUIAutomation::get_ReservedMixedAttributeValue, ReservedMixedAttributeValue property [Windows Accessibility], ReservedMixedAttributeValue property [Windows Accessibility],IUIAutomation interface, get_ReservedMixedAttributeValue, uiauto.uiauto_IUIAutomation_ReservedMixedAttributeValue, uiauto_IUIAutomation_ReservedMixedAttributeValue, uiautomationclient/IUIAutomation::ReservedMixedAttributeValue, uiautomationclient/IUIAutomation::get_ReservedMixedAttributeValue, winauto.uiauto_IUIAutomation_ReservedMixedAttributeValue
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
 - IUIAutomation::get_ReservedMixedAttributeValue
 - uiautomationclient/IUIAutomation::get_ReservedMixedAttributeValue
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
 - IUIAutomation.ReservedMixedAttributeValue
 - IUIAutomation.get_ReservedMixedAttributeValue
---

# IUIAutomation::get_ReservedMixedAttributeValue


## -description

Retrieves a static token object representing a text attribute that is a mixed attribute.

This property is read-only.

## -parameters

## -remarks

 The object retrieved by <b>IUIAutomation::ReservedMixedAttributeValue</b> can be used for comparison with the results from <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue">IUIAutomationTextRange::GetAttributeValue</a> to determine if a text range contains more than one value for a particular text attribute.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation">IUIAutomation</a>



<a href="/windows/desktop/WinAuto/uiauto-textattributes">UI Automation Text Attributes</a>