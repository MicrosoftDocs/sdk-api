---
UID: NF:windows.foundation.IPropertyValue.GetDateTime
title: IPropertyValue::IPropertyValue (windows.foundation.h)
description: Gets the DateTime value that is stored in the current IPropertyValue object.
helpviewer_keywords: ["GetDateTime","GetDateTime method [Windows Runtime]","GetDateTime method [Windows Runtime]","IPropertyValue interface","IPropertyValue interface [Windows Runtime]","GetDateTime method","IPropertyValue.GetDateTime","IPropertyValue.IPropertyValue","IPropertyValue::GetDateTime","IPropertyValue::IPropertyValue","windows/IPropertyValue::GetDateTime","winrt.ipropertyvalue_getdatetime"]
old-location: winrt\ipropertyvalue_getdatetime.htm
tech.root: WinRT
ms.assetid: 3ffe8778-ce0e-46bb-9387-48c20d5dddfc
ms.date: 12/05/2018
ms.keywords: GetDateTime, GetDateTime method [Windows Runtime], GetDateTime method [Windows Runtime],IPropertyValue interface, IPropertyValue interface [Windows Runtime],GetDateTime method, IPropertyValue.GetDateTime, IPropertyValue.IPropertyValue, IPropertyValue::GetDateTime, IPropertyValue::IPropertyValue, windows/IPropertyValue::GetDateTime, winrt.ipropertyvalue_getdatetime
req.header: windows.foundation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Windows.Foundation.idl
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
 - IPropertyValue::GetDateTime
 - windows.foundation/IPropertyValue::GetDateTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windows.Foundation.h
api_name:
 - IPropertyValue.GetDateTime
---

# IPropertyValue::IPropertyValue


## -description

Gets the <a href="/windows/desktop/api/windows.foundation/ns-windows-foundation-datetime">DateTime</a> value that is stored in the current <a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> object.

## -parameters

### -param value [out, retval]

Type: <b><a href="/windows/desktop/api/windows.foundation/ns-windows-foundation-datetime">DateTime</a>*</b>

The value.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a>



<a href="/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvaluestatics-createdatetime">IPropertyValueStatics::CreateDateTime</a>