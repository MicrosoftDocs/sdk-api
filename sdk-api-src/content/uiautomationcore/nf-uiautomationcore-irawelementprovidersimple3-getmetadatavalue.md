---
UID: NF:uiautomationcore.IRawElementProviderSimple3.GetMetadataValue
title: IRawElementProviderSimple3::GetMetadataValue (uiautomationcore.h)
description: Gets metadata from the UI Automation element that indicates how the information should be interpreted. (IRawElementProviderSimple3.GetMetadataValue)
helpviewer_keywords: ["GetMetadataValue","GetMetadataValue method [Windows Accessibility]","GetMetadataValue method [Windows Accessibility]","IRawElementProviderSimple3 interface","IRawElementProviderSimple3 interface [Windows Accessibility]","GetMetadataValue method","IRawElementProviderSimple3.GetMetadataValue","IRawElementProviderSimple3::GetMetadataValue","uiautomationcore/IRawElementProviderSimple3::GetMetadataValue","winauto.uiauto_IRawElementProviderSimple3_GetMetadataValue"]
old-location: winauto\uiauto_IRawElementProviderSimple3_GetMetadataValue.htm
tech.root: WinAuto
ms.assetid: 832154F3-22D3-48E9-BC4E-CB495BB72485
ms.date: 12/05/2018
ms.keywords: GetMetadataValue, GetMetadataValue method [Windows Accessibility], GetMetadataValue method [Windows Accessibility],IRawElementProviderSimple3 interface, IRawElementProviderSimple3 interface [Windows Accessibility],GetMetadataValue method, IRawElementProviderSimple3.GetMetadataValue, IRawElementProviderSimple3::GetMetadataValue, uiautomationcore/IRawElementProviderSimple3::GetMetadataValue, winauto.uiauto_IRawElementProviderSimple3_GetMetadataValue
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: None supported
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
req.dll: UIAutomationCore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRawElementProviderSimple3::GetMetadataValue
 - uiautomationcore/IRawElementProviderSimple3::GetMetadataValue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.dll
api_name:
 - IRawElementProviderSimple3.GetMetadataValue
---

# IRawElementProviderSimple3::GetMetadataValue


## -description

Gets metadata from the UI Automation element that indicates how the information should be interpreted. For example, should the string "1/4" be interpreted as a fraction or a date?

## -parameters

### -param targetId [in]

The ID of the property to retrieve.

### -param metadataId [in]

Specifies the type of metadata to retrieve.

### -param returnVal [out, retval]

The metadata.

## -returns

Returns <b>S_OK</b> if successful, otherwise an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementprovidersimple3">IRawElementProviderSimple3</a>



<a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-sayasinterpretas">SayAsInterpretAs</a>
