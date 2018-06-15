---
UID: NF:propsys.PSFormatForDisplay
title: PSFormatForDisplay function
author: windows-sdk-content
description: Gets a formatted, Unicode string representation of a property value stored in a PROPVARIANT structure. The caller is responsible for allocating the output buffer.
old-location: properties\PSFormatForDisplay.htm
old-project: properties
ms.assetid: 71442967-ee8a-448c-83cf-949934ddd152
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: PSFormatForDisplay, PSFormatForDisplay function [Windows Properties], properties.PSFormatForDisplay, propsys/PSFormatForDisplay, shell.PSFormatForDisplay, shell_PSFormatForDisplay
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: PSC_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - PSFormatForDisplay
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PSFormatForDisplay function


## -description


Gets a formatted, Unicode string representation of a property value stored in a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure. The caller is responsible for allocating the output buffer.


## -parameters




### -param propkey [in]

Type: <b>REFPROPERTYKEY</b>

Reference to a <a href="https://www.bing.com/search?q=PROPERTYKEY">PROPERTYKEY</a> that names the property whose value is being retrieved.


### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure that contains the type and value of the property.


### -param pdfFlags [in]

Type: <b><a href="/windows/desktop/api/propsys/ne-propsys-propdesc_format_flags">PROPDESC_FORMAT_FLAGS</a></b>

A flag that specifies the format to apply to the property string. See <a href="/windows/desktop/api/propsys/ne-propsys-propdesc_format_flags">PROPDESC_FORMAT_FLAGS</a> for possible values.


### -param pwszText [out]

Type: <b>LPWSTR</b>

When the function returns, contains a pointer to the formatted value as a null-terminated, Unicode string. The calling application is responsible for allocating memory for the buffer before it calls <a href="https://www.bing.com/search?q=PSFormatForDisplay">PSFormatForDisplay</a>.


### -param cchText [in]

Type: <b>DWORD</b>

Specifies the length of the buffer at <i>pwszText</i> in <b>WCHAR</b><b>s</b>, including the terminating null character.


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
The formatted string was successfully created.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The formatted string was not created. S_FALSE indicates that an empty string resulted from a VT_EMPTY.

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



This function calls the schema subsystem's implementation of <a href="/windows/desktop/api/propsys/nf-propsys-ipropertysystem-formatfordisplay">IPropertySystem::FormatForDisplay</a>. That call provides a Unicode string representation of a property value, with additional formatting based on one or more <a href="/windows/desktop/api/propsys/ne-propsys-propdesc_format_flags">PROPDESC_FORMAT_FLAGS</a>. If the <a href="https://www.bing.com/search?q=PROPERTYKEY">PROPERTYKEY</a> is not recognized by the schema subsystem, <b>IPropertySystem::FormatForDisplay</b> attempts to format the value according to the value's <a href="https://msdn.microsoft.com/library/windows/desktop/317b911b-1805-402d-a9cb-159546bc88b4">VARTYPE</a>.

You must initialize Component Object Model (COM) with <a href="https://msdn.microsoft.com/0f171cf4-87b9-43a6-97f2-80ed344fe376">CoInitialize</a> or <a href="https://msdn.microsoft.com/9a13e7a0-f2e2-466b-98f5-38d5972fa391">OleInitialize</a> before you call <a href="https://www.bing.com/search?q=PSFormatPropertyValue">PSFormatPropertyValue</a>.

The purpose of this function is to convert data into a string suitable for display to the user. The value is formatted according to the current locale, the language of the user, the <a href="/windows/desktop/api/propsys/ne-propsys-propdesc_format_flags">PROPDESC_FORMAT_FLAGS</a>, and the property description specified by the property key. For information on how the property description schema influences the formatting of the value, see the following topics:
                
                

<ul>
<li>
<a href="https://www.bing.com/search?q=displayInfo">displayInfo</a>
</li>
<li>
<a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">stringFormat</a>
</li>
<li>
<a href="https://www.bing.com/search?q=booleanFormat">booleanFormat</a>
</li>
<li>
<a href="https://www.bing.com/search?q=numberFormat">numberFormat</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3ed64cf2-d6f3-4ad0-9194-838e82df7472">NMDATETIMEFORMAT</a>
</li>
<li>
<a href="https://www.bing.com/search?q=enumeratedList">enumeratedList</a>
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
<td>The following file attributes are converted to letters and appended to create a string (for example, a value of 0x1801 is converted to "RCO"):</td>
</tr>
<tr>
<td> </td>
<td>FILE_ATTRIBUTE_READONLY- 'R'</td>
</tr>
<tr>
<td> </td>
<td>FILE_ATTRIBUTE_SYSTEM - 'S'</td>
</tr>
<tr>
<td> </td>
<td>FILE_ATTRIBUTE_ARCHIVE -'A'</td>
</tr>
<tr>
<td> </td>
<td>FILE_ATTRIBUTE_COMPRESSED - 'C'</td>
</tr>
<tr>
<td> </td>
<td>FILE_ATTRIBUTE_ENCRYPTED - 'E'</td>
</tr>
<tr>
<td> </td>
<td>FILE_ATTRIBUTE_OFFLINE - 'O'</td>
</tr>
<tr>
<td> </td>
<td>FILE_ATTRIBUTE_NOT_CONTENT_INDEXED - 'I'</td>
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

The following example, to be included as part of a larger program, demonstrates how to use <a href="https://www.bing.com/search?q=PSFormatForDisplay">PSFormatForDisplay</a> to format a rating value.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>PROPVARIANT propvar;

HRESULT hr = InitPropVariantFromUInt32(RATING_THREE_STARS_SET, &amp;propvar);

if (SUCCEEDED(hr))
{
    WCHAR szValue[100];

    hr = PSFormatForDisplay(PKEY_Rating, propvar, PDFF_DEFAULT, szValue, ARRAYSIZE(szValue));

    if (SUCCEEDED(hr))
    {
        // szValue contains a formatted string similar to "3 stars".
    }
    PropVariantClear(&amp;propvar);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://www.bing.com/search?q=PSFormatForDisplayAlloc">PSFormatForDisplayAlloc</a>



<a href="https://www.bing.com/search?q=PSFormatPropertyValue">PSFormatPropertyValue</a>



<a href="https://msdn.microsoft.com/cac93c31-d90d-4116-b846-0cf593d1d56e">Property Description Schema</a>
 

 

