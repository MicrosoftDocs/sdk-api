---
UID: NF:propsys.IPropertyDescription.FormatForDisplay
title: IPropertyDescription::FormatForDisplay
author: windows-sdk-content
description: Gets a formatted, Unicode string representation of a property value.
old-location: properties\IPropertyDescription_FormatForDisplay.htm
tech.root: properties
ms.assetid: c900fce9-4462-4429-a5a1-9f0d1e73c681
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: FormatForDisplay, FormatForDisplay method [Windows Properties], FormatForDisplay method [Windows Properties],IPropertyDescription interface, IPropertyDescription interface [Windows Properties],FormatForDisplay method, IPropertyDescription.FormatForDisplay, IPropertyDescription::FormatForDisplay, properties.IPropertyDescription_FormatForDisplay, propsys/IPropertyDescription::FormatForDisplay, shell.IPropertyDescription_FormatForDisplay, shell_IPropertyDescription_FormatForDisplay
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.h
api_name:
 - IPropertyDescription.FormatForDisplay
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- propsys.h
: 
- IPropertyDescription.FormatForDisplay
: 
---

# IPropertyDescription::FormatForDisplay


## -description


Gets a formatted, Unicode string representation of a property value.


## -parameters




### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

A reference to a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure that contains the type and value of the property.


### -param pdfFlags [in]

Type: <b><a href="shell.PROPDESC_FORMAT_FLAGS">PROPDESC_FORMAT_FLAGS</a></b>

One or more of the <a href="shell.PROPDESC_FORMAT_FLAGS">PROPDESC_FORMAT_FLAGS</a> flags, which are either bitwise or multiple values, that indicate the property string format.


### -param ppszDisplay

TBD




#### - cchText [out]

Type: <b>DWORD</b>

The length of the buffer at <i>pszText</i> in WCHARS, including the terminating <b>NULL</b>. The maximum size is 0x8000 (32K).


#### - key [in]

Type: <b>REFPROPERTYKEY</b>

A reference to the requested property key, which identifies a property. See <a href="shell.PROPERTYKEY">PROPERTYKEY</a>.


#### - pszText [out]

Type: <b>LPWSTR*</b>

When this method returns, contains the formatted value as a <b>null</b>-terminated, Unicode string. The calling application must allocate memory for the buffer, and use <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> to release the string specified by <i>pszText</i> when it is no longer needed.


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



You must initialize Component Object Model (COM) with <a href="https://msdn.microsoft.com/0f171cf4-87b9-43a6-97f2-80ed344fe376">CoInitialize</a> or <a href="https://msdn.microsoft.com/9a13e7a0-f2e2-466b-98f5-38d5972fa391">OleInitialize</a> before calling <a href="shell.IPropertyDescription_FormatForDisplay">IPropertyDescription::FormatForDisplay</a>.

On success, this method gets a formatted Unicode string representation of a property value for a specified <a href="shell.PROPERTYKEY">PROPERTYKEY</a>, and one or more <a href="shell.PROPDESC_FORMAT_FLAGS">PROPDESC_FORMAT_FLAGS</a>.

The purpose of this method is to convert data into a string suitable for display to the user. The value is formatted according to the current locale, the language of the user, the <a href="shell.PROPDESC_FORMAT_FLAGS">PROPDESC_FORMAT_FLAGS</a>, and the property description specified by the property key. For information about how the property description schema influences the formatting of the value, see <a href="shell.propdesc_schema_displayInfo">displayInfo</a>, <a href="shell.propdesc_schema_stringFormat">stringFormat</a>, <a href="shell.propdesc_schema_booleanFormat">booleanFormat</a>, <a href="shell.propdesc_schema_numberFormat">numberFormat</a>, <a href="https://msdn.microsoft.com/3ed64cf2-d6f3-4ad0-9194-838e82df7472">NMDATETIMEFORMAT</a>,  and <a href="shell.propdesc_schema_enumeratedList">enumeratedList</a>. Typically, the <b>PROPDESC_FORMAT_FLAGS</b> are used to modify the format prescribed by the property description.

The output string can contain Unicode directional characters. These nonspacing characters influence the Unicode bidirectional algorithm so that the values appear correctly when a left to right (LTR) language is drawn on an right to left (RTL) window, and vice versa. These characters include the following: <code>"\x200e", "\x200f", "\x202a", "\x202b", "\x202c", "\x202d", "\x202e".</code>

The following properties use special formats and are unaffected by the <a href="shell.PROPDESC_FORMAT_FLAGS">PROPDESC_FORMAT_FLAGS</a> (examples cited are for strings with a current locale set to English; typically, output is localized except where noted).

<table class="clsStd">
<tr>
<th>Property</th>
<th>Format</th>
</tr>
<tr>
<td>
<a href="shell.props_System_FileAttributes">System.FileAttributes</a>
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
<a href="shell.props_System_Photo_ISOSpeed">System.Photo.ISOSpeed</a>
</td>
<td>For example, "ISO-400".</td>
</tr>
<tr>
<td>
<a href="shell.props_System_Photo_ShutterSpeed">System.Photo.ShutterSpeed</a>
</td>
<td>
The APEX value is converted to an exposure time using this formula:

<code>Exposure_time = 2^(-APEX_value)</code>

For example, "2 sec."or "1/125 sec.".

</td>
</tr>
<tr>
<td>
<a href="shell.props_System_Photo_ExposureTime">System.Photo.ExposureTime</a>
</td>
<td>For example,  "2 sec."or "1/125 sec." </td>
</tr>
<tr>
<td>
<a href="shell.props_System_Photo_Aperture">System.Photo.Aperture</a>
</td>
<td>
The APEX value is converted to an F number using this formula:

<code>F_Number = 2^(APEX_Value / 2)</code>

For example, "f/5.6".

</td>
</tr>
<tr>
<td>
<a href="shell.props_System_Photo_FNumber">System.Photo.FNumber</a>
</td>
<td>For example,  "f/5.6".</td>
</tr>
<tr>
<td>
<a href="shell.props_System_Photo_SubjectDistance">System.Photo.SubjectDistance</a>
</td>
<td>For example, "15 m"or "250 mm".</td>
</tr>
<tr>
<td>
<a href="shell.props_System_Photo_FocalLength">System.Photo.FocalLength</a>
</td>
<td>For example,  "50 mm".</td>
</tr>
<tr>
<td>
<a href="shell.props_System_Photo_FlashEnergy">System.Photo.FlashEnergy</a>
</td>
<td>For example,  "500 bpcs".</td>
</tr>
<tr>
<td>
<a href="shell.props_System_Photo_ExposureBias">System.Photo.ExposureBias</a>
</td>
<td>For example, "-2 step", " 0 step", or "+3 step".</td>
</tr>
<tr>
<td>
<a href="shell.props_System_Computer_DecoratedFreeSpace">System.Computer.DecoratedFreeSpace</a>
</td>
<td>For example, "105 MB free of 13.2 GB".</td>
</tr>
<tr>
<td>
<a href="shell.props_System_ItemType">System.ItemType</a>
</td>
<td>For example, "Application" or "JPEG Image".</td>
</tr>
<tr>
<td>
<a href="shell.props_System_ComputerName">System.ComputerName</a>
</td>
<td>For example, "LITWARE05 (this computer)" or "testbox07".</td>
</tr>
</table>
 




## -see-also




<a href="shell.IPropertyDescription">IPropertyDescription</a>



<a href="https://msdn.microsoft.com/cac93c31-d90d-4116-b846-0cf593d1d56e">Property Description Schema</a>
 

 

