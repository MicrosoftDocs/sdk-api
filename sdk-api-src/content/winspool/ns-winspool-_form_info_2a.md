---
UID: NS:winspool._FORM_INFO_2A
title: "_FORM_INFO_2A"
author: windows-driver-content
description: Contains information about a localizable print form.
old-location: gdi\form_info_2.htm
old-project: printdocs
ms.assetid: 5cc11a77-2b9d-44a4-88de-6ed0b7460bc8
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*LPFORM_INFO_2A, *PFORM_INFO_2A, FORM_INFO_2, FORM_INFO_2 structure [Windows GDI], FORM_INFO_2A, PFORM_INFO_2, PFORM_INFO_2 structure pointer [Windows GDI], _FORM_INFO_2A, _FORM_INFO_2W, _win32_FORM_INFO_2_str, gdi.form_info_2, winspool/FORM_INFO_2, winspool/PFORM_INFO_2, winspool/_FORM_INFO_2A, winspool/_FORM_INFO_2W"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winspool.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: "_FORM_INFO_2W (Unicode) and _FORM_INFO_2A (ANSI)"
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: FORM_INFO_2A, *PFORM_INFO_2A, *LPFORM_INFO_2A
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winspool.h
api_name:
-	FORM_INFO_2
-	_FORM_INFO_2A
-	_FORM_INFO_2W
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _FORM_INFO_2A structure


## -description



Contains information about a localizable print form.




## -struct-fields




### -field Flags

The form properties. The following values are defined, but only one can be set. When the <b>FORM_INFO_2</b> is returned by <a href="https://msdn.microsoft.com/10b25748-6d7c-46ab-bd2c-9b6126a1d7d1">GetForm</a> or <a href="https://msdn.microsoft.com/b13b515a-c764-4a80-ab85-95fb4abb2a6b">EnumForms</a>, <b>Flags</b> is set to the current value in the forms database.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>FORM_USER</td>
<td>If this bit flag is set, the form has been defined by the user. Forms with this flag set are defined in the registry.</td>
</tr>
<tr>
<td>FORM_BUILTIN</td>
<td>If this bit-flag is set, the form is part of the spooler. Form definitions with this flag set do not appear in the registry. Built-in forms cannot be modified, so this flag should not be set when the structure is passed to <a href="https://msdn.microsoft.com/17b59019-f93a-4b57-86fb-91c61aecbac4">AddForm</a> or <a href="https://msdn.microsoft.com/05d5d495-952c-4a1d-8694-1004d0c2bcf6">SetForm</a>.</td>
</tr>
<tr>
<td>FORM_PRINTER</td>
<td>If this bit flag is set, the form is associated with a certain printer, and its definition appears in the registry.</td>
</tr>
</table>
 


### -field pName

A pointer to a null-terminated string that specifies the name of the form. The form name cannot exceed 31 characters.


### -field Size

The width and height of the form in thousandths of millimeters.


### -field ImageableArea

The width and height, in thousandths of millimeters, of the area of the page on which the printer can print.


### -field pKeyword

A pointer to a non-localizable string identifier of the form. When passed to <a href="https://msdn.microsoft.com/17b59019-f93a-4b57-86fb-91c61aecbac4">AddForm</a> or <a href="https://msdn.microsoft.com/05d5d495-952c-4a1d-8694-1004d0c2bcf6">SetForm</a>, this gives the caller a means of identifying the form in all locales.


### -field StringType

Specifies how a localized display name for the form is obtained at runtime. The following values are defined. Only one can be set in any given call to <a href="https://msdn.microsoft.com/17b59019-f93a-4b57-86fb-91c61aecbac4">AddForm</a> or <a href="https://msdn.microsoft.com/05d5d495-952c-4a1d-8694-1004d0c2bcf6">SetForm</a>. Both STRING_MUIDLL and STRING_LANGPAIR can be set in the <b>FORM_INFO_2</b> (s) returned by <a href="https://msdn.microsoft.com/10b25748-6d7c-46ab-bd2c-9b6126a1d7d1">GetForm</a> or <a href="https://msdn.microsoft.com/b13b515a-c764-4a80-ab85-95fb4abb2a6b">EnumForms</a>. See Remarks.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>STRING_NONE</td>
<td>There is no localized display name.</td>
</tr>
<tr>
<td>STRING_MUIDLL</td>
<td>The display name is extracted from the <a href="https://msdn.microsoft.com/4d8b769d-0830-4e4e-b284-ce0b21dfe5d4">Multilingual User Interface</a> localized resources DLL specified in <b>pMuiDll</b>. The ID is in the <b>dwResourceId</b> member.</td>
</tr>
<tr>
<td>STRING_LANGPAIR</td>
<td>The display name and language ID are provided directly by <b>pDisplayName</b> and the language is specified by <b>wLangId</b>.</td>
</tr>
</table>
 


### -field pMuiDll

The <a href="https://msdn.microsoft.com/4d8b769d-0830-4e4e-b284-ce0b21dfe5d4">Multilingual User Interface</a> localized resource DLL that contains the localized display name.


### -field dwResourceId

The resource ID of the form's display name in <b>pMuiDll</b>.


### -field pDisplayName

The form's display name in the language specified by <b>wLangId</b>.


### -field wLangId

The language of the <b>pDisplayName</b>.


## -remarks



On a call to <a href="https://msdn.microsoft.com/17b59019-f93a-4b57-86fb-91c61aecbac4">AddForm</a> or <a href="https://msdn.microsoft.com/05d5d495-952c-4a1d-8694-1004d0c2bcf6">SetForm</a>:

<ul>
<li>If <b>StringType</b> is STRING_NONE, both <b>pMuiDll</b> and <b>pDisplayName</b> must be <b>NULL</b> and both <b>dwResourceId</b> and <b>wLangId</b> must be 0.</li>
<li>If <b>StringType</b> is STRING_MUIDLL, <b>pDisplayName</b> must be <b>NULL</b> and <b>wLangId</b> must be 0.</li>
<li>If <b>StringType</b> is STRING_LANGPAIR, <b>pMuiDll</b> must be <b>NULL</b> and <b>dwResourceId</b> must be 0.</li>
</ul>
For a <b>FORM_INFO_2</b> returned by a call to <a href="https://msdn.microsoft.com/10b25748-6d7c-46ab-bd2c-9b6126a1d7d1">GetForm</a> or <a href="https://msdn.microsoft.com/b13b515a-c764-4a80-ab85-95fb4abb2a6b">EnumForms</a>:

<ul>
<li>If <b>StringType</b> is both STRING_MUIDLL and STRING_LANGPAIR, <b>pMuiDll</b>, <b>pDisplayName</b>, <b>dwResourceId</b>, and <b>wLangId</b> will all have valid values.</li>
<li>If <b>StringType</b> is STRING_MUIDLL only, <b>pMuiDll</b> and <b>dwResourceId</b> will have valid values. <b>pDisplayName</b> will be <b>NULL</b> and <b>wLangId</b> will be 0.</li>
<li>If <b>StringType</b> is STRING_LANGPAIR only, <b>pDisplayName</b> and <b>wLangId</b> will have valid values. <b>pMuiDll</b> will be <b>NULL</b> and <b>dwResourceId</b> will be 0.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/17b59019-f93a-4b57-86fb-91c61aecbac4">AddForm</a>



<a href="https://msdn.microsoft.com/b13b515a-c764-4a80-ab85-95fb4abb2a6b">EnumForms</a>



<a href="https://msdn.microsoft.com/10b25748-6d7c-46ab-bd2c-9b6126a1d7d1">GetForm</a>



<a href="https://msdn.microsoft.com/4d8b769d-0830-4e4e-b284-ce0b21dfe5d4">Multilingual User Interface
</a>



<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>



<a href="https://msdn.microsoft.com/05d5d495-952c-4a1d-8694-1004d0c2bcf6">SetForm</a>
 

 

