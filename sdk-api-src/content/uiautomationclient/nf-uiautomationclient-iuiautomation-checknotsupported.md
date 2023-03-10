---
UID: NF:uiautomationclient.IUIAutomation.CheckNotSupported
title: IUIAutomation::CheckNotSupported (uiautomationclient.h)
description: Checks a provided VARIANT to see if it contains the Not Supported identifier.
helpviewer_keywords: ["CheckNotSupported","CheckNotSupported method [Windows Accessibility]","CheckNotSupported method [Windows Accessibility]","IUIAutomation interface","IUIAutomation interface [Windows Accessibility]","CheckNotSupported method","IUIAutomation.CheckNotSupported","IUIAutomation::CheckNotSupported","uiauto.uiauto_IUIAutomation_CheckNotSupported","uiauto_IUIAutomation_CheckNotSupported","uiautomationclient/IUIAutomation::CheckNotSupported","winauto.uiauto_IUIAutomation_CheckNotSupported"]
old-location: winauto\uiauto_IUIAutomation_CheckNotSupported.htm
tech.root: WinAuto
ms.assetid: c7fd7d1e-3f7b-4700-9263-2cab6e0de896
ms.date: 12/05/2018
ms.keywords: CheckNotSupported, CheckNotSupported method [Windows Accessibility], CheckNotSupported method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],CheckNotSupported method, IUIAutomation.CheckNotSupported, IUIAutomation::CheckNotSupported, uiauto.uiauto_IUIAutomation_CheckNotSupported, uiauto_IUIAutomation_CheckNotSupported, uiautomationclient/IUIAutomation::CheckNotSupported, winauto.uiauto_IUIAutomation_CheckNotSupported
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
 - IUIAutomation::CheckNotSupported
 - uiautomationclient/IUIAutomation::CheckNotSupported
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
 - IUIAutomation.CheckNotSupported
---

# IUIAutomation::CheckNotSupported


## -description

Checks a provided <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> to see if it contains the Not Supported identifier.

## -parameters

### -param value [in]

Type: <b><a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a></b>

The value to check.

### -param isNotSupported [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a>*</b>

Receives <b>TRUE</b> if the provided <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> contains the Not Supported identifier, or <b>FALSE</b> otherwise.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

After retrieving a property for a UI Automation element, call this method to determine whether the element supports the retrieved property. <b>CheckNotSupported</b> is typically called after calling a property retrieving method such as <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue">GetCurrentPropertyValue</a>.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation">IUIAutomation</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-get_reservednotsupportedvalue">IUIAutomation::ReservedNotSupportedValue</a>