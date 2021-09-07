---
UID: NF:windows.foundation.IPropertyValue.GetGuid
title: IPropertyValue::GetGuid (windows.foundation.h)
description: Gets the GUID value that is stored in the current IPropertyValue object.
helpviewer_keywords: ["GetGuid","GetGuid method [Windows Runtime]","GetGuid method [Windows Runtime]","IPropertyValue interface","IPropertyValue interface [Windows Runtime]","GetGuid method","IPropertyValue.GetGuid","IPropertyValue.IPropertyValue","IPropertyValue::GetGuid","IPropertyValue::IPropertyValue","windows/IPropertyValue::GetGuid","winrt.ipropertyvalue_getguid"]
old-location: winrt\ipropertyvalue_getguid.htm
tech.root: WinRT
ms.assetid: d094f70f-dfd3-4601-b288-4f9f79479609
ms.date: 12/05/2018
ms.keywords: GetGuid, GetGuid method [Windows Runtime], GetGuid method [Windows Runtime],IPropertyValue interface, IPropertyValue interface [Windows Runtime],GetGuid method, IPropertyValue.GetGuid, IPropertyValue.IPropertyValue, IPropertyValue::GetGuid, IPropertyValue::IPropertyValue, windows/IPropertyValue::GetGuid, winrt.ipropertyvalue_getguid
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
 - IPropertyValue::GetGuid
 - windows.foundation/IPropertyValue::GetGuid
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
 - IPropertyValue.GetGuid
---

# IPropertyValue::GetGuid (windows.foundation.h)


## -description

Gets the GUID value that is stored in the current <a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> object.

## -parameters

### -param value [out, retval]

Type: <b>GUID*</b>

The value.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a>



<a href="/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvaluestatics-createguid">IPropertyValueStatics::CreateGuid</a>
