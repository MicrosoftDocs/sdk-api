---
UID: NF:propsys.IPropertySystem.FormatForDisplay
title: IPropertySystem::FormatForDisplay (propsys.h)
description: Gets a formatted, Unicode string representation of a property value. (IPropertySystem.FormatForDisplay)
helpviewer_keywords: ["FormatForDisplay","FormatForDisplay method [Windows Properties]","FormatForDisplay method [Windows Properties]","IPropertySystem interface","IPropertySystem interface [Windows Properties]","FormatForDisplay method","IPropertySystem.FormatForDisplay","IPropertySystem::FormatForDisplay","properties.IPropertySystem_FormatForDisplay","propsys/IPropertySystem::FormatForDisplay","shell.IPropertySystem_FormatForDisplay","shell_IPropertySystem_FormatForDisplay"]
old-location: properties\IPropertySystem_FormatForDisplay.htm
tech.root: properties
ms.assetid: 674b1651-6354-4995-abeb-271df3748e1b
ms.date: 12/05/2018
ms.keywords: FormatForDisplay, FormatForDisplay method [Windows Properties], FormatForDisplay method [Windows Properties],IPropertySystem interface, IPropertySystem interface [Windows Properties],FormatForDisplay method, IPropertySystem.FormatForDisplay, IPropertySystem::FormatForDisplay, properties.IPropertySystem_FormatForDisplay, propsys/IPropertySystem::FormatForDisplay, shell.IPropertySystem_FormatForDisplay, shell_IPropertySystem_FormatForDisplay
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
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - IPropertySystem::FormatForDisplay
 - propsys/IPropertySystem::FormatForDisplay
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
 - IPropertySystem.FormatForDisplay
---

# IPropertySystem::FormatForDisplay


## -description

Gets a formatted, Unicode string representation of a property value.

## -parameters

### -param key [in]

Type: <b>REFPROPERTYKEY</b>

A reference to the requested <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">property key</a>.

### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

A reference to a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure containing the type and value of the property.

### -param pdff [in]

Type: <b><a href="/windows/desktop/api/propsys/ne-propsys-propdesc_format_flags">PROPDESC_FORMAT_FLAGS</a></b>

The format of the property string. See <a href="/windows/desktop/api/propsys/ne-propsys-propdesc_format_flags">PROPDESC_FORMAT_FLAGS</a> for possible values.

### -param pszText [out]

Type: <b>LPWSTR</b>

Receives the formatted value as a null-terminated, Unicode string. The calling application must allocate memory for the buffer.

### -param cchText [in]

Type: <b>DWORD</b>

The length of the buffer at  <i>pszText</i> in <b>WCHAR</b><b>s</b>, including the terminating <b>NULL</b>. The maximum size is 0x8000 (32K).

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
Formatted string is created.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Formatted string is not created. S_FALSE indicates that the empty string resulted from a VT_EMPTY.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Memory allocation failed.

</td>
</tr>
</table>

## -remarks

You must initialize Component Object Model (COM) with <a href="/windows/desktop/api/objbase/nf-objbase-coinitialize">CoInitialize</a> or <a href="/windows/desktop/api/ole2/nf-ole2-oleinitialize">OleInitialize</a> before calling <a href="/windows/desktop/api/propsys/nf-propsys-ipropertysystem-formatfordisplay">IPropertySystem::FormatForDisplay</a>.

When it succeeds, this method gets a formatted Unicode string representation of a property value for a specified <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a>, and one or more <a href="/windows/desktop/api/propsys/ne-propsys-propdesc_format_flags">PROPDESC_FORMAT_FLAGS</a>. If the <b>PROPERTYKEY</b> is not recognized by the schema subsystem, <a href="/windows/desktop/api/propsys/nf-propsys-ipropertysystem-formatfordisplay">IPropertySystem::FormatForDisplay</a> attempts to format the value according to its <a href="/previous-versions/windows/desktop/legacy/ms221127(v=vs.85)">VARTYPE</a>.

The purpose of this method is to convert data into a string suitable for display to the user. The value is formatted according to the current locale, the language of the user, the <a href="/windows/desktop/api/propsys/ne-propsys-propdesc_format_flags">PROPDESC_FORMAT_FLAGS</a>, and the property description specified by the property key. For information about how the property description schema influences the formatting of the value, see <a href="/windows/desktop/properties/propdesc-schema-displayinfo">displayInfo</a>, <a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">stringFormat</a>, <a href="/windows/desktop/properties/propdesc-schema-booleanformat">booleanFormat</a>, <a href="/windows/desktop/properties/propdesc-schema-numberformat">numberFormat</a>, <a href="/windows/desktop/api/commctrl/ns-commctrl-nmdatetimeformata">NMDATETIMEFORMAT</a>,  and <a href="/windows/desktop/properties/propdesc-schema-enumeratedlist">enumeratedList</a>.  Typically, the <b>PROPDESC_FORMAT_FLAGS</b> are used to modify the format prescribed by the property description.

The output string may contain Unicode directional characters.  These nonspacing characters influence the Unicode bidirectional algorithm so that the values appear correctly when a left-to-right (LTR) language is drawn on a right-to-left (RTL) window, and vice versa.  These characters include the following: <code>"\x200e", "\x200f", "\x202a", "\x202b", "\x202c", "\x202d", "\x202e".</code>

The properties in the following table use special formats and are unaffected by the <a href="/windows/desktop/api/propsys/ne-propsys-propdesc_format_flags">PROPDESC_FORMAT_FLAGS</a> (examples cited are for strings with a current locale set to English; typically, output is localized except where noted).

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
<td>For example,  "2 sec."or "1/125 sec." </td>
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
<td>For example,  "50 mm".</td>
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
 

If the property key does not correspond to a property description in any of the registered property schemas, this method chooses a format based on the type of the value, as described in the following table.

<table class="clsStd">
<tr>
<th><b>Type of the value</b></th>
<th><b>Format</b></th>
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
<td>Decimal string in the current locale. For example, "42".</td>
</tr>
<tr>
<td>VT_LPWSTR or other</td>
<td>String. Sequences of "\r", "\t", or "\n" are replaced with a single space.</td>
</tr>
<tr>
<td>VT_VECTOR | anything</td>
<td>Semicolon separated values—a semicolon is used regardless of locale.</td>
</tr>
</table>
