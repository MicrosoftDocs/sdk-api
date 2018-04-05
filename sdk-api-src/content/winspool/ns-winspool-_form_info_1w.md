---
UID: NS:winspool._FORM_INFO_1W
title: "_FORM_INFO_1W"
author: windows-driver-content
description: The FORM_INFO_1 structure contains information about a print form. The information includes the print form's origin, its name, its dimensions, and the dimensions of its printable area.
old-location: gdi\form_info_1.htm
old-project: printdocs
ms.assetid: 1c42ea6c-82cf-463c-bc67-44a8d8c4a1e7
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*LPFORM_INFO_1W, *PFORM_INFO_1W, FORM_INFO_1, FORM_INFO_1 structure [Windows GDI], FORM_INFO_1W, PFORM_INFO_1, PFORM_INFO_1 structure pointer [Windows GDI], _FORM_INFO_1A, _FORM_INFO_1W, _win32_FORM_INFO_1_str, gdi.form_info_1, winspool/FORM_INFO_1, winspool/PFORM_INFO_1, winspool/_FORM_INFO_1A, winspool/_FORM_INFO_1W"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winspool.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: "_FORM_INFO_1W (Unicode) and _FORM_INFO_1A (ANSI)"
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: FORM_INFO_1W, *PFORM_INFO_1W, *LPFORM_INFO_1W
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winspool.h
api_name:
-	FORM_INFO_1
-	_FORM_INFO_1A
-	_FORM_INFO_1W
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _FORM_INFO_1W structure


## -description



The <b>FORM_INFO_1</b> structure contains information about a print form. The information includes the print form's origin, its name, its dimensions, and the dimensions of its printable area.




## -struct-fields




### -field Flags

The form properties. The following values are defined.

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
<td>If this bit-flag is set, the form is part of the spooler. Form definitions with this flag set do not appear in the registry.</td>
</tr>
<tr>
<td>FORM_PRINTER</td>
<td>If this bit flag is set, the form is associated with a certain printer, and its definition appears in the registry.</td>
</tr>
</table>
 


### -field pName

Pointer to a null-terminated string that specifies the name of the form. The form name cannot exceed 31 characters.


### -field Size

The width and height, in thousandths of millimeters, of the form.


### -field ImageableArea

The width and height, in thousandths of millimeters, of the form.


## -see-also




<a href="https://msdn.microsoft.com/17b59019-f93a-4b57-86fb-91c61aecbac4">AddForm</a>



<a href="https://msdn.microsoft.com/10b25748-6d7c-46ab-bd2c-9b6126a1d7d1">GetForm</a>



<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>



<a href="https://msdn.microsoft.com/05d5d495-952c-4a1d-8694-1004d0c2bcf6">SetForm</a>
 

 

