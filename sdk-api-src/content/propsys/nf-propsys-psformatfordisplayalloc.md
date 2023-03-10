---
UID: NF:propsys.PSFormatForDisplayAlloc
title: PSFormatForDisplayAlloc function (propsys.h)
description: Gets a formatted, Unicode string representation of a property value stored in a PROPVARIANT structure. This function allocates memory for the output string.
helpviewer_keywords: ["PSFormatForDisplayAlloc","PSFormatForDisplayAlloc function [Windows Properties]","properties.PSFormatForDisplayAlloc","propsys/PSFormatForDisplayAlloc","shell.PSFormatForDisplayAlloc","shell_PSFormatForDisplayAlloc"]
old-location: properties\PSFormatForDisplayAlloc.htm
tech.root: properties
ms.assetid: d411ea72-fb29-47b6-a7f6-0839b3e2caf2
ms.date: 12/05/2018
ms.keywords: PSFormatForDisplayAlloc, PSFormatForDisplayAlloc function [Windows Properties], properties.PSFormatForDisplayAlloc, propsys/PSFormatForDisplayAlloc, shell.PSFormatForDisplayAlloc, shell_PSFormatForDisplayAlloc
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
 - PSFormatForDisplayAlloc
 - propsys/PSFormatForDisplayAlloc
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
 - PSFormatForDisplayAlloc
---

# PSFormatForDisplayAlloc function


## -description

Gets a formatted, Unicode string representation of a property value stored in a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure. This function allocates memory for the output string.

## -parameters

### -param key [in]

Type: <b>REFPROPERTYKEY</b>

Reference to a <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> that names the property whose value is being retrieved.

### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure that contains the type and value of the property.

### -param pdff [in]

Type: <b><a href="/windows/desktop/api/propsys/ne-propsys-propdesc_format_flags">PROPDESC_FORMAT_FLAGS</a></b>

One or more flags that specify the format to apply to the property string. See <a href="/windows/desktop/api/propsys/ne-propsys-propdesc_format_flags">PROPDESC_FORMAT_FLAGS</a> for possible values.

### -param ppszDisplay [out]

Type: <b>PWSTR*</b>

When the function returns, contains a pointer to a null-terminated, Unicode string representation of the requested property value.

## -returns

Type: <b>HRESULT</b>

Returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The formatted string was successfully created. <b>S_OK</b> together with an empty return string indicates that there was an empty input string or a non-empty value that was formatted as an empty string.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The formatted string was not created. S_FALSE together with an empty return string indicates that the empty string resulted from a VT_EMPTY.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Indicates allocation failed.

</td>
</tr>
</table>

## -remarks

This function calls the schema subsystem's implementation of <a href="/windows/desktop/api/propsys/nf-propsys-ipropertysystem-formatfordisplayalloc">IPropertySystem::FormatForDisplayAlloc</a>. That call provides a Unicode string representation of a property value, with additional formatting based on one or more <a href="/windows/desktop/api/propsys/ne-propsys-propdesc_format_flags">PROPDESC_FORMAT_FLAGS</a>. If the <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> is not recognized by the schema subsystem, <b>IPropertySystem::FormatForDisplayAlloc</b> attempts to format the value according to the value's <a href="/previous-versions/windows/desktop/legacy/ms221127(v=vs.85)">VARTYPE</a>.

You must initialize Component Object Model (COM) with <a href="/windows/desktop/api/objbase/nf-objbase-coinitialize">CoInitialize</a> or <a href="/windows/desktop/api/ole2/nf-ole2-oleinitialize">OleInitialize</a> before you call <a href="/windows/desktop/api/propsys/nf-propsys-psformatfordisplayalloc">PSFormatForDisplayAlloc</a>.

The function allocates memory through <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a> and returns a pointer to that memory through the <i>ppszDisplay</i> parameter. The calling application must use <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> to release that resource when it is no longer needed.

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

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propsys/nf-propsys-psformatfordisplayalloc">PSFormatForDisplayAlloc</a> to format a rating value.


```cpp
PROPVARIANT propvar;

HRESULT hr = InitPropVariantFromUInt32(RATING_THREE_STARS_SET, &propvar);

if (SUCCEEDED(hr))
{
    PWSTR pszValue;

    hr = PSFormatForDisplayAlloc(PKEY_Rating, propvar, PDFF_DEFAULT, &pszValue);

    if (SUCCEEDED(hr))
    {
        // pszValue contains a formatted string similar to "3 stars".
         CoTaskMemFree(pszValue);
    }
    PropVariantClear(&propvar);
}
```

## -see-also

<a href="/windows/desktop/api/propsys/nf-propsys-psformatfordisplay">PSFormatForDisplay</a>



<a href="/windows/desktop/api/propsys/nf-propsys-psformatpropertyvalue">PSFormatPropertyValue</a>



<a href="/windows/desktop/properties/propdesc-schema-entry">Property Description Schema</a>