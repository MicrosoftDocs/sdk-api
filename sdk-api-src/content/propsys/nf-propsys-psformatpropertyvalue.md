---
UID: NF:propsys.PSFormatPropertyValue
title: PSFormatPropertyValue function (propsys.h)
description: Gets a formatted, Unicode string representation of a property value stored in a property store. This function allocates memory for the output string.
old-location: properties\PSFormatPropertyValue.htm
tech.root: properties
ms.assetid: 35c2b424-05bd-4d7d-8365-5900e165e2e2
ms.date: 12/05/2018
ms.keywords: PSFormatPropertyValue, PSFormatPropertyValue function [Windows Properties], _shell_PSFormatPropertyValue, properties.PSFormatPropertyValue, propsys/PSFormatPropertyValue, shell.PSFormatPropertyValue
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - PSFormatPropertyValue
 - propsys/PSFormatPropertyValue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - PSFormatPropertyValue
---

# PSFormatPropertyValue function


## -description

Gets a formatted, Unicode string representation of a property value stored in a property store. This function allocates memory for the output string.

## -parameters

### -param pps [in]

Type: <b><a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a>*</b>

Pointer to an <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a>, which represents the property store from which the property value is taken.

### -param ppd [in]

Type: <b><a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescription">IPropertyDescription</a>*</b>

Pointer to an <a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescription">IPropertyDescription</a>, which represents the property whose value is being retrieved.

### -param pdff [in]

Type: <b><a href="/windows/desktop/api/propsys/ne-propsys-propdesc_format_flags">PROPDESC_FORMAT_FLAGS</a></b>

One or more <a href="/windows/desktop/api/propsys/ne-propsys-propdesc_format_flags">PROPDESC_FORMAT_FLAGS</a> that specify the format to apply to the property string. See <b>PROPDESC_FORMAT_FLAGS</b> for possible values.

### -param ppszDisplay [out]

Type: <b>LPWSTR*</b>

When the function returns, contains a pointer to the formatted value as a null-terminated, Unicode string.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function uses the <i>ppd</i> parameter to call <a href="/windows/desktop/api/propsys/nf-propsys-ipropertydescription-formatfordisplay">IPropertyDescription::FormatForDisplay</a>. That call provides a Unicode string representation of a property value, with additional formatting based on one or more <a href="/windows/desktop/api/propsys/ne-propsys-propdesc_format_flags">PROPDESC_FORMAT_FLAGS</a>.

You must initialize Component Object Model (COM) with <a href="/windows/desktop/api/objbase/nf-objbase-coinitialize">CoInitialize</a> or <a href="/windows/desktop/api/ole2/nf-ole2-oleinitialize">OleInitialize</a> before you call <a href="/windows/desktop/api/propsys/nf-propsys-psformatpropertyvalue">PSFormatPropertyValue</a>.

The function allocates memory and returns a pointer to that memory in <i>ppszDisplay</i>. The calling application must use <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> to release the string specified by <i>ppszDisplay</i> when it is no longer needed.

The purpose of this function is to convert data into a string suitable for display to the user. The value is formatted according to the current locale, the language of the user, the <a href="/windows/desktop/api/propsys/ne-propsys-propdesc_format_flags">PROPDESC_FORMAT_FLAGS</a>, and the property description specified by the property key. For information on how the property description schema influences the formatting of the value, see the following topics:
                
                

<ul>
<li>
<a href="/windows/desktop/properties/propdesc-schema-displayinfo">displayInfo</a>
</li>
<li>
<a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">stringFormat</a>
</li>
<li>
<a href="/windows/desktop/properties/propdesc-schema-booleanformat">booleanFormat</a>
</li>
<li>
<a href="/windows/desktop/properties/propdesc-schema-numberformat">numberFormat</a>
</li>
<li>
<a href="/windows/desktop/api/commctrl/ns-commctrl-nmdatetimeformata">NMDATETIMEFORMAT</a>
</li>
<li>
<a href="/windows/desktop/properties/propdesc-schema-enumeratedlist">enumeratedList</a>
</li>
</ul>
 
            
                Typically, the <b>PROPDESC_FORMAT_FLAGS</b> are used to modify the format prescribed by the property description.
            

The output string can contain Unicode directional characters. These nonspacing characters influence the Unicode bidirectional algorithm so that the values appear correctly when a left-to-right (LTR) language is drawn on a right-to-left (RTL) window, or an RTL is drawn on a LTR window. These characters include the following: <code>"\x200e", "\x200f", "\x202a", "\x202b", "\x202c", "\x202d", "\x202e".</code>

The following properties use special formats and are unaffected by the <a href="/windows/desktop/api/propsys/ne-propsys-propdesc_format_flags">PROPDESC_FORMAT_FLAGS</a>. Note that examples cited are for strings with a current locale set to English; typically, output is localized except where noted.

                

<table class="clsStd">
<tr>
<th>Property</th>
<th>Format</th>
</tr>
<tr>
<td>System.FileAttributes</td>
<td>The following file attributes are converted to letters and appended to create a string (for example, a value of 0x1801 (FILE_ATTRIBUTE_READONLY | FILE_ATTRIBUTE_COMPRESSED | FILE_ATTRIBUTE_OFFLINE) is converted to "RCO"):
                            
                            <ul>
<li>FILE_ATTRIBUTE_READONLY (0x00000001) - 'R'</li>
<li>FILE_ATTRIBUTE_SYSTEM (0x00000004) - 'S'</li>
<li>FILE_ATTRIBUTE_ARCHIVE (0x00000020) -'A'</li>
<li>FILE_ATTRIBUTE_COMPRESSED (0x00000800) - 'C'</li>
<li>FILE_ATTRIBUTE_ENCRYPTED (0x00004000) - 'E'</li>
<li>FILE_ATTRIBUTE_OFFLINE (0x00001000) - 'O'</li>
<li>FILE_ATTRIBUTE_NOT_CONTENT_INDEXED (0x00002000) - 'I'</li>
</ul>
</td>
</tr>
<tr>
<td>System.Photo.ISOSpeed</td>
<td>For example, "ISO-400".</td>
</tr>
<tr>
<td>System.Photo.ShutterSpeed</td>
<td>
The APEX value is converted to an exposure time using this formula:

<code>Exposure_time = 2^(-APEX_value)</code>

For example, "2 sec."or "1/125 sec.".

</td>
</tr>
<tr>
<td>System.Photo.ExposureTime</td>
<td>For example, "2 sec."or "1/125 sec." </td>
</tr>
<tr>
<td>System.Photo.Aperture</td>
<td>
The APEX value is converted to an F number using this formula:

<code>F_Number = 2^(APEX_Value / 2)</code>

For example, "f/5.6".

</td>
</tr>
<tr>
<td>System.Photo.FNumber</td>
<td>For example, "f/5.6".</td>
</tr>
<tr>
<td>System.Photo.SubjectDistance</td>
<td>For example, "15 m"or "250 mm".</td>
</tr>
<tr>
<td>System.Photo.FocalLength</td>
<td>For example, "50 mm".</td>
</tr>
<tr>
<td>System.Photo.FlashEnergy</td>
<td>For example, "500 bpcs".</td>
</tr>
<tr>
<td>System.Photo.ExposureBias</td>
<td>For example, "-2 step", " 0 step", or "+3 step".</td>
</tr>
<tr>
<td>System.Computer.DecoratedFreeSpace</td>
<td>For example, "105 MB free of 13.2 GB".</td>
</tr>
<tr>
<td>System.ItemType</td>
<td>For example, "Application" or "JPEG Image".</td>
</tr>
<tr>
<td>System.ControlPanel.Category</td>
<td>For example, "Appearance and Personalization".</td>
</tr>
<tr>
<td>System.ComputerName</td>
<td>For example, "LITWARE05 (this computer)" or "testbox07".</td>
</tr>
</table>
 

If the property key does not correspond to a property description in any of the registered property schemas, then this function chooses a format based on the type of the value.

<table class="clsStd">
<tr>
<th>Type of the value</th>
<th>Format</th>
</tr>
<tr>
<td>VT_BOOLEAN</td>
<td>Not supported.</td>
</tr>
<tr>
<td>VT_FILETIME</td>
<td>Date/time string as specified by <a href="/windows/desktop/api/propsys/ne-propsys-propdesc_format_flags">PROPDESC_FORMAT_FLAGS</a> and the current locale. PDFF_SHORTTIME and PDFF_SHORTDATE are the default. For example, "11/13/2006 3:22 PM".</td>
</tr>
<tr>
<td>Numeric VARTYPE</td>
<td>Decimal string in the current locale. For example, "42". </td>
</tr>
<tr>
<td>VT_LPWSTR or other</td>
<td>Converted to a string. Sequences of "\r", "\t", or "\n" are replaced with a single space.</td>
</tr>
<tr>
<td>VT_VECTOR | anything</td>
<td>Semicolon separated values. A semicolon is used regardless of locale.</td>
</tr>
</table>
 


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propsys/nf-propsys-psformatpropertyvalue">PSFormatPropertyValue</a> to format a rating value.


```cpp
// IPropertyStore *pStore;
// Assume the variable pps is initialized and valid.
IPropertyDescription *pPropDesc;

HRESULT hr = PSGetPropertyDescription(PKEY_Rating, IID_PPV_ARGS(&pPropDesc));

if (SUCCEEDED(hr))
{
    PWSTR pszValue;

    hr = PSFormatPropertyValue(pStore, pPropDesc, PDFF_DEFAULT, &pszValue);

    if (SUCCEEDED(hr))
    {
        // pszValue contains a formatted string similar to "3 stars".
        CoTaskMemFree(pszValue);
    }
    pPropDesc->Release();
}
```

## -see-also

<a href="/windows/desktop/api/propsys/nf-propsys-psformatfordisplay">PSFormatForDisplay</a>



<a href="/windows/desktop/api/propsys/nf-propsys-psformatfordisplayalloc">PSFormatForDisplayAlloc</a>



<a href="/windows/desktop/properties/propdesc-schema-entry">Property Description Schema</a>