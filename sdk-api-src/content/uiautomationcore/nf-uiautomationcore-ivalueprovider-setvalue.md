---
UID: NF:uiautomationcore.IValueProvider.SetValue
title: IValueProvider::SetValue (uiautomationcore.h)
description: Sets the value of control.
helpviewer_keywords: ["IValueProvider interface [Windows Accessibility]","SetValue method","IValueProvider.SetValue","IValueProvider::SetValue","SetValue","SetValue method [Windows Accessibility]","SetValue method [Windows Accessibility]","IValueProvider interface","uiauto.uiauto_IValueProvider_SetValue","uiauto_IValueProvider_SetValue","uiautomationcore/IValueProvider::SetValue","winauto.uiauto_IValueProvider_SetValue"]
old-location: winauto\uiauto_IValueProvider_SetValue.htm
tech.root: WinAuto
ms.assetid: af555ac6-5abd-4019-804b-68f9ed3be801
ms.date: 12/05/2018
ms.keywords: IValueProvider interface [Windows Accessibility],SetValue method, IValueProvider.SetValue, IValueProvider::SetValue, SetValue, SetValue method [Windows Accessibility], SetValue method [Windows Accessibility],IValueProvider interface, uiauto.uiauto_IValueProvider_SetValue, uiauto_IValueProvider_SetValue, uiautomationcore/IValueProvider::SetValue, winauto.uiauto_IValueProvider_SetValue
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
 - IValueProvider::SetValue
 - uiautomationcore/IValueProvider::SetValue
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
 - IValueProvider.SetValue
---

# IValueProvider::SetValue


## -description

Sets the value of control.

## -parameters

### -param val [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCWSTR</a></b>

The value to set. The provider is responsible for converting the value to the appropriate data type.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Single-line edit controls support programmatic access to their contents by implementing <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ivalueprovider">IValueProvider</a>. 
        However, multi-line edit controls do not implement <b>IValueProvider</b>; 
        instead they provide access to their content by implementing <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider">ITextProvider</a>.
        

Controls such as ListItem and TreeItem must implement <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ivalueprovider">IValueProvider</a> 
        if the value of any of the items is editable, regardless of the current edit 
        mode of the control. The parent control must also implement <b>IValueProvider</b> 
        if the child items are editable.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ivalueprovider">IValueProvider</a>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>