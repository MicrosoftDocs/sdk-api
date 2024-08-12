---
UID: NF:dwrite_3.IDWriteFontFace5.GetFontAxisValues
title: IDWriteFontFace5::GetFontAxisValues
description: Retrieves the list of axis values used by the font.
helpviewer_keywords: ["IDWriteFontFace5 interface [Direct Write]","GetFontAxisValues method","IDWriteFontFace5.GetFontAxisValues","IDWriteFontFace5::GetFontAxisValues","GetFontAxisValues","GetFontAxisValues method [Direct Write]","GetFontAxisValues method [Direct Write]","IDWriteFontFace5 interface","directwrite.idwritefontface5_getfontaxisvalues","dwrite_3/IDWriteFontFace5::GetFontAxisValues"]
tech.root: DirectWrite
ms.date: 09/10/2019
ms.keywords: IDWriteFontFace5 interface [Direct Write],GetFontAxisValues method, IDWriteFontFace5.GetFontAxisValues, IDWriteFontFace5::GetFontAxisValues, GetFontAxisValues, GetFontAxisValues method [Direct Write], GetFontAxisValues method [Direct Write],IDWriteFontFace5 interface, directwrite.idwritefontface5_getfontaxisvalues, dwrite_3/IDWriteFontFace5::GetFontAxisValues
req.construct-type: function
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 16299
req.target-min-winversvr: Windows 10 Build 16299
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwrite.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - IDWriteFontFace5::GetFontAxisValues
 - dwrite_3/IDWriteFontFace5::GetFontAxisValues
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dwrite.lib
 - Dwrite.dll
api_name:
 - IDWriteFontFace5::GetFontAxisValues
---

## -description

Retrieves the list of axis values used by the font.

## -parameters

### -param fontAxisValues [out]

Type: **[DWRITE_FONT_AXIS_VALUE](./ns-dwrite_3-dwrite_font_axis_value.md)\***

A pointer to an array of **DWRITE_FONT_AXIS_VALUE** structures into which **GetFontAxisValues** writes the list of font axis values. You're responsible for managing the size and the lifetime of this array. Call [GetFontAxisValueCount](./nf-dwrite_3-idwritefontface5-getfontaxisvaluecount.md) to determine the size of array to allocate.

### -param fontAxisValueCount

Type: **[UINT32](/windows/win32/winprog/windows-data-types)**

The maximum number of font axis values to write into the memory block pointed to by `fontAxisValues`.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

|Return value|Description|
|-|-|
|E_INVALIDARG|`fontAxisValueCount` doesn't match the value returned by **GetFontAxisValueCount**.|

## -remarks

The values are returned in the canonical order defined by the font, clamped to the actual range supported. It's not necessarily the same axis value array that you passed to **CreateFontFace**.

## Examples

```cppwinrt
// main.cpp
#include <unknwn.h>
#include <winrt/base.h>
#include <dwrite_3.h>

int main()
{
	winrt::init_apartment();

	winrt::com_ptr<IDWriteFactory> factory;

	winrt::check_hresult(::DWriteCreateFactory(
		DWRITE_FACTORY_TYPE_SHARED,
		__uuidof(factory),
		reinterpret_cast<IUnknown**>(factory.put())));

	std::wstring filePath{ L"C:\\WINDOWS\\FONTS\\AGENCYB.TTF" };

	winrt::com_ptr<IDWriteFontFile> fontFile;

	factory->CreateFontFileReference(
		filePath.c_str(),
		nullptr,
		fontFile.put());

	std::array<IDWriteFontFile*, 1> fontFiles{ fontFile.get() };

	winrt::com_ptr<IDWriteFontFace> fontFace;

	winrt::check_hresult(factory->CreateFontFace(
		DWRITE_FONT_FACE_TYPE_TRUETYPE,
		1,
		fontFiles.data(),
		0,
		DWRITE_FONT_SIMULATIONS_NONE,
		fontFace.put()
	));

	winrt::com_ptr<IDWriteFontFace5> fontFace5{ fontFace.as<IDWriteFontFace5>() };
	
	UINT32 axisValueCount{ fontFace5->GetFontAxisValueCount() };

	DWRITE_FONT_AXIS_VALUE* axisValues{ new DWRITE_FONT_AXIS_VALUE[axisValueCount] };

	winrt::check_hresult(
		fontFace5->GetFontAxisValues(axisValues, axisValueCount));

	DWRITE_FONT_AXIS_VALUE* eachAxisValue{ axisValues };

	for (int ix = 0; ix < axisValueCount; ++ix, ++eachAxisValue)
	{
		printf("%zu,%f\n\r", eachAxisValue->axisTag, eachAxisValue->value);
	}

	delete[] axisValues;
}
```

## -see-also
