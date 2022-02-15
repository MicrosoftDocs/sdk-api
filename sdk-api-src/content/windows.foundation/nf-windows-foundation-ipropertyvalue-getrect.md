---
UID: NF:windows.foundation.IPropertyValue.GetRect
title: IPropertyValue::GetRect (windows.foundation.h)
description: Gets the Rect value that is stored in the current IPropertyValue object.
helpviewer_keywords: ["GetRect","GetRect method [Windows Runtime]","GetRect method [Windows Runtime]","IPropertyValue interface","IPropertyValue interface [Windows Runtime]","GetRect method","IPropertyValue.GetRect","IPropertyValue.IPropertyValue","IPropertyValue::GetRect","IPropertyValue::IPropertyValue","windows/IPropertyValue::GetRect","winrt.ipropertyvalue_getrect"]
old-location: winrt\ipropertyvalue_getrect.htm
tech.root: WinRT
ms.assetid: 2333bd80-56db-4fa4-b696-269969fd1362
ms.date: 12/05/2018
ms.keywords: GetRect, GetRect method [Windows Runtime], GetRect method [Windows Runtime],IPropertyValue interface, IPropertyValue interface [Windows Runtime],GetRect method, IPropertyValue.GetRect, IPropertyValue.IPropertyValue, IPropertyValue::GetRect, IPropertyValue::IPropertyValue, windows/IPropertyValue::GetRect, winrt.ipropertyvalue_getrect
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
 - IPropertyValue::GetRect
 - windows.foundation/IPropertyValue::GetRect
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
 - IPropertyValue.GetRect
---

# IPropertyValue::GetRect (windows.foundation.h)


## -description

Gets the <a href="/windows/desktop/api/windows.foundation/ns-windows-foundation-rect">Rect</a> value that is stored in the current <a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> object.

## -parameters

### -param value [out, retval]

Type: <b><a href="/windows/desktop/api/windows.foundation/ns-windows-foundation-rect">Rect</a>*</b>

The value.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a>



<a href="/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvaluestatics-createrect">IPropertyValueStatics::CreateRect</a>
