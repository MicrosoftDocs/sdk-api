---
UID: NF:propsys.IPropertyDescription.FormatForDisplay
title: IPropertyDescription::FormatForDisplay (propsys.h)
description: Gets a formatted, Unicode string representation of a property value. (IPropertyDescription.FormatForDisplay)
old-location: properties\IPropertyDescription_FormatForDisplay.htm
tech.root: properties
ms.assetid: c900fce9-4462-4429-a5a1-9f0d1e73c681
ms.date: 12/05/2018
ms.keywords: FormatForDisplay, FormatForDisplay method [Windows Properties], FormatForDisplay method [Windows Properties],IPropertyDescription interface, IPropertyDescription interface [Windows Properties],FormatForDisplay method, IPropertyDescription.FormatForDisplay, IPropertyDescription::FormatForDisplay, properties.IPropertyDescription_FormatForDisplay, propsys/IPropertyDescription::FormatForDisplay, shell.IPropertyDescription_FormatForDisplay, shell_IPropertyDescription_FormatForDisplay
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
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
 - IPropertyDescription::FormatForDisplay
 - propsys/IPropertyDescription::FormatForDisplay
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.h
api_name:
 - IPropertyDescription.FormatForDisplay
---

# IPropertyDescription::FormatForDisplay


## -description

Gets a formatted, Unicode string representation of a property value.

## -parameters

### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

A reference to a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure that contains the type and value of the property.

### -param pdfFlags [in]

Type: <b><a href="/windows/desktop/api/propsys/ne-propsys-propdesc_format_flags">PROPDESC_FORMAT_FLAGS</a></b>

One or more of the <a href="/windows/desktop/api/propsys/ne-propsys-propdesc_format_flags">PROPDESC_FORMAT_FLAGS</a> flags, which are either bitwise or multiple values, that indicate the property string format.

### -param ppszDisplay [out]

Type: <b>LPWSTR*</b>

The address of a pointer to a null-terminated Unicode string that contains the display text.

#### - cchText [out]

Type: <b>DWORD</b>

The length of the buffer at <i>pszText</i> in WCHARS, including the terminating <b>NULL</b>. The maximum size is 0x8000 (32K).


#### - key [in]

Type: <b>REFPROPERTYKEY</b>

A reference to the requested property key, which identifies a property. See <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a>.


#### - pszText [out]

Type: <b>LPWSTR*</b>

When this method returns, contains the formatted value as a <b>null</b>-terminated, Unicode string. The calling application must allocate memory for the buffer, and use <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> to release the string specified by <i>pszText</i> when it is no longer needed.

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
The string was copied and <b>null</b>-terminated without truncation. This string may be returned empty due to an empty input string or from a non-empty value that was formatted as an empty string.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The empty string resulted from a VT_EMPTY.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pszText</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The copy operation failed due to insufficient space. The destination buffer is modified to contain a truncated version of the ideal result and is <b>null</b>-terminated.

</td>
</tr>
</table>

## -remarks

You must initialize Component Object Model (COM) with <a href="/windows/desktop/api/objbase/nf-objbase-coinitialize">CoInitialize</a> or <a href="/windows/desktop/api/ole2/nf-ole2-oleinitialize">OleInitialize</a> before calling <a href="/windows/desktop/api/propsys/nf-propsys-ipropertydescription-formatfordisplay">IPropertyDescription::FormatForDisplay</a>.

On success, this method gets a formatted Unicode string representation of a property value for a specified <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a>, and one or more <a href="/windows/desktop/api/propsys/ne-propsys-propdesc_format_flags">PROPDESC_FORMAT_FLAGS</a>.

The purpose of this method is to convert data into a string suitable for display to the user. The value is formatted according to the current locale, the language of the user, the <a href="/windows/desktop/api/propsys/ne-propsys-propdesc_format_flags">PROPDESC_FORMAT_FLAGS</a>, and the property description specified by the property key. For information about how the property description schema influences the formatting of the value, see <a href="/windows/desktop/properties/propdesc-schema-displayinfo">displayInfo</a>, <a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">stringFormat</a>, <a href="/windows/desktop/properties/propdesc-schema-booleanformat">booleanFormat</a>, <a href="/windows/desktop/properties/propdesc-schema-numberformat">numberFormat</a>, <a href="/windows/desktop/api/commctrl/ns-commctrl-nmdatetimeformata">NMDATETIMEFORMAT</a>,  and <a href="/windows/desktop/properties/propdesc-schema-enumeratedlist">enumeratedList</a>. Typically, the <b>PROPDESC_FORMAT_FLAGS</b> are used to modify the format prescribed by the property description.

The output string can contain Unicode directional characters. These nonspacing characters influence the Unicode bidirectional algorithm so that the values appear correctly when a left-to-right (LTR) language is drawn onto a right-to-left (RTL) window, and vice versa. These characters include the following: <code>"\x200e", "\x200f", "\x202a", "\x202b", "\x202c", "\x202d", "\x202e".</code>

The following properties use special formats and are unaffected by the <a href="/windows/desktop/api/propsys/ne-propsys-propdesc_format_flags">PROPDESC_FORMAT_FLAGS</a> (examples cited are for strings with a current locale set to English; typically, output is localized except where noted).

<table class="clsStd">
<tr>
<th>Property</th>
<th>Format</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/properties/props-system-fileattributes">System.FileAttributes</a>
</td>
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
<td>
<a href="/windows/desktop/properties/props-system-photo-isospeed">System.Photo.ISOSpeed</a>
</td>
<td>For example, "ISO-400".</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/properties/props-system-photo-shutterspeed">System.Photo.ShutterSpeed</a>
</td>
<td>
The APEX value is converted to an exposure time using this formula:

<code>Exposure_time = 2^(-APEX_value)</code>

For example, "2 sec."or "1/125 sec.".

</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/properties/props-system-photo-exposuretime">System.Photo.ExposureTime</a>
</td>
<td>For example,  "2 sec."or "1/125 sec." </td>
</tr>
<tr>
<td>
<a href="/windows/desktop/properties/props-system-photo-aperture">System.Photo.Aperture</a>
</td>
<td>
The APEX value is converted to an F number using this formula:

<code>F_Number = 2^(APEX_Value / 2)</code>

For example, "f/5.6".

</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/properties/props-system-photo-fnumber">System.Photo.FNumber</a>
</td>
<td>For example,  "f/5.6".</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/properties/props-system-photo-subjectdistance">System.Photo.SubjectDistance</a>
</td>
<td>For example, "15 m"or "250 mm".</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/properties/props-system-photo-focallength">System.Photo.FocalLength</a>
</td>
<td>For example,  "50 mm".</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/properties/props-system-photo-flashenergy">System.Photo.FlashEnergy</a>
</td>
<td>For example,  "500 bpcs".</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/properties/props-system-photo-exposurebias">System.Photo.ExposureBias</a>
</td>
<td>For example, "-2 step", " 0 step", or "+3 step".</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/properties/props-system-computer-decoratedfreespace">System.Computer.DecoratedFreeSpace</a>
</td>
<td>For example, "105 MB free of 13.2 GB".</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/properties/props-system-itemtype">System.ItemType</a>
</td>
<td>For example, "Application" or "JPEG Image".</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/properties/props-system-computername">System.ComputerName</a>
</td>
<td>For example, "LITWARE05 (this computer)" or "testbox07".</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescription">IPropertyDescription</a>



<a href="/windows/desktop/properties/propdesc-schema-entry">Property Description Schema</a>
