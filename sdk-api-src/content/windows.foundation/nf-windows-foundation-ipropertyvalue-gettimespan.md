---
UID: NF:windows.foundation.IPropertyValue.GetTimeSpan
title: IPropertyValue::GetTimeSpan (windows.foundation.h)
description: Gets the TimeSpan value that is stored in the current IPropertyValue object.
helpviewer_keywords: ["GetTimeSpan","GetTimeSpan method [Windows Runtime]","GetTimeSpan method [Windows Runtime]","IPropertyValue interface","IPropertyValue interface [Windows Runtime]","GetTimeSpan method","IPropertyValue.GetTimeSpan","IPropertyValue.IPropertyValue","IPropertyValue::GetTimeSpan","IPropertyValue::IPropertyValue","windows/IPropertyValue::GetTimeSpan","winrt.ipropertyvalue_gettimespan"]
old-location: winrt\ipropertyvalue_gettimespan.htm
tech.root: WinRT
ms.assetid: c78d584f-e2ef-4623-b45a-e26d2ec1518b
ms.date: 12/05/2018
ms.keywords: GetTimeSpan, GetTimeSpan method [Windows Runtime], GetTimeSpan method [Windows Runtime],IPropertyValue interface, IPropertyValue interface [Windows Runtime],GetTimeSpan method, IPropertyValue.GetTimeSpan, IPropertyValue.IPropertyValue, IPropertyValue::GetTimeSpan, IPropertyValue::IPropertyValue, windows/IPropertyValue::GetTimeSpan, winrt.ipropertyvalue_gettimespan
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
 - IPropertyValue::GetTimeSpan
 - windows.foundation/IPropertyValue::GetTimeSpan
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
 - IPropertyValue.GetTimeSpan
---

# IPropertyValue::GetTimeSpan (windows.foundation.h)


## -description

Gets the <a href="/windows/desktop/api/windows.foundation/ns-windows-foundation-timespan">TimeSpan</a> value that is stored in the current <a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> object.

## -parameters

### -param value [out, retval]

Type: <b><a href="/windows/desktop/api/windows.foundation/ns-windows-foundation-timespan">TimeSpan</a>*</b>

The value.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a>



<a href="/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvaluestatics-createtimespan">IPropertyValueStatics::CreateTimeSpan</a>
