---
UID: NF:windows.foundation.IPropertyValue.GetTimeSpanArray
title: IPropertyValue::IPropertyValue (windows.foundation.h)
description: Gets the array of TimeSpan values that is stored in the current IPropertyValue object.
helpviewer_keywords: ["GetTimeSpanArray","GetTimeSpanArray method [Windows Runtime]","GetTimeSpanArray method [Windows Runtime]","IPropertyValue interface","IPropertyValue interface [Windows Runtime]","GetTimeSpanArray method","IPropertyValue.GetTimeSpanArray","IPropertyValue.IPropertyValue","IPropertyValue::GetTimeSpanArray","IPropertyValue::IPropertyValue","windows/IPropertyValue::GetTimeSpanArray","winrt.ipropertyvalue_gettimespanarray"]
old-location: winrt\ipropertyvalue_gettimespanarray.htm
tech.root: WinRT
ms.assetid: a52a665c-4c3a-4489-bd7b-e8ecb8dfe9cc
ms.date: 12/05/2018
ms.keywords: GetTimeSpanArray, GetTimeSpanArray method [Windows Runtime], GetTimeSpanArray method [Windows Runtime],IPropertyValue interface, IPropertyValue interface [Windows Runtime],GetTimeSpanArray method, IPropertyValue.GetTimeSpanArray, IPropertyValue.IPropertyValue, IPropertyValue::GetTimeSpanArray, IPropertyValue::IPropertyValue, windows/IPropertyValue::GetTimeSpanArray, winrt.ipropertyvalue_gettimespanarray
f1_keywords:
- windows.foundation/IPropertyValue.GetTimeSpanArray
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Windows.Foundation.h
api_name:
- IPropertyValue.GetTimeSpanArray
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPropertyValue::IPropertyValue


## -description


Gets the array of <a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/ns-windows-foundation-timespan">TimeSpan</a> values that is stored in the current <a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> object.


## -parameters




### -param __valueSize [out]

Type: <b>UINT32*</b>

The number of values in the array.


### -param value [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/ns-windows-foundation-timespan">TimeSpan</a>**</b>

The array of <a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/ns-windows-foundation-timespan">TimeSpan</a> values.

The returned pointer must be freed using <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvaluestatics-createtimespanarray">IPropertyValueStatics::CreateTimeSpanArray</a>
 

 

