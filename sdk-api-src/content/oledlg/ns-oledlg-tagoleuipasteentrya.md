---
UID: NS:oledlg.tagOLEUIPASTEENTRYA
title: tagOLEUIPASTEENTRYA
author: windows-sdk-content
description: An array of entries to be specified in the OLEUIPASTESPECIAL structure for the Paste Special dialog box.
old-location: com\oleuipasteentry_struct.htm
old-project: com
ms.assetid: 9c84bb0e-d998-4e35-bf34-2377f5cd0cb7
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: "*LPOLEUIPASTEENTRYA, *POLEUIPASTEENTRYA, LPOLEUIPASTEENTRY, LPOLEUIPASTEENTRY structure pointer [COM], OLEUIPASTEENTRY, OLEUIPASTEENTRY structure [COM], OLEUIPASTEENTRYA, OLEUIPASTEENTRYW, POLEUIPASTEENTRY, POLEUIPASTEENTRY structure pointer [COM], _ole_OLEUIPASTEENTRY, com.oleuipasteentry_struct, oledlg/LPOLEUIPASTEENTRY, oledlg/OLEUIPASTEENTRY, oledlg/OLEUIPASTEENTRYA, oledlg/OLEUIPASTEENTRYW, oledlg/POLEUIPASTEENTRY, tagOLEUIPASTEENTRYA"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: oledlg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OLEUIPASTEENTRYW (Unicode) and OLEUIPASTEENTRYA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: OLEUIPASTEENTRYA, *POLEUIPASTEENTRYA, *LPOLEUIPASTEENTRYA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OleDlg.h
api_name:
 - OLEUIPASTEENTRY
 - OLEUIPASTEENTRYA
 - OLEUIPASTEENTRYW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# tagOLEUIPASTEENTRYA structure


## -description


An array of entries to be specified in the <a href="https://msdn.microsoft.com/bb346fa7-03ae-458d-8488-64db7a9c48e1">OLEUIPASTESPECIAL</a> structure for the <b>Paste Special</b> dialog box. Each entry includes a <a href="https://msdn.microsoft.com/4478eb9a-84a1-4f3a-8290-94b8dd20c081">FORMATETC</a> structure which specifies the formats that are acceptable, a string that is to represent the format in the dialog box's listbox, a string to customize the result text of the dialog box, and a set of flags from the <a href="https://msdn.microsoft.com/4467f82b-34be-4d10-816c-b3e4231c92a1">OLEUIPASTEFLAG</a> enumeration. The flags indicate if the entry is valid for pasting only, linking only or both pasting and linking. If the entry is valid for linking, the flags indicate which link types are acceptable by OR'ing together the appropriate OLEUIPASTE_LINKTYPE<i>n</i> values.


## -struct-fields




### -field fmtetc

Format that is acceptable. The <b>Paste Special</b> dialog box checks if this format is offered by the object on the clipboard and if so, offers it for selection to the user.


### -field lpstrFormatName

Pointer to the string that represents the format to the user. Any %s in this string is replaced by the FullUserTypeName of the object on the clipboard and the resulting string is placed in the list box of the dialog box. Only one %s is allowed. The presence or absence of %s specifies whether the result-text is to indicate that data is being pasted or that an object that can be activated by an application is being pasted. If %s is present, the resulting text says that an object is being pasted. Otherwise, it says that data is being pasted.


### -field lpstrResultText

Pointer to the string used to customize the resulting text of the dialog box when the user selects the format corresponding to this entry. Any %s in this string is replaced by the application name or FullUserTypeName of the object on the clipboard. Only one %s is allowed.


### -field dwFlags

Values from <a href="https://msdn.microsoft.com/4467f82b-34be-4d10-816c-b3e4231c92a1">OLEUIPASTEFLAG</a> enumeration.


### -field dwScratchSpace

Scratch space available to routines that loop through an <a href="https://msdn.microsoft.com/4d180fdd-2d58-4d26-9242-6552dda0d3e6">IEnumFORMATETC</a> to mark if the PasteEntry format is available. This field can be left uninitialized.



## -see-also




<a href="https://msdn.microsoft.com/4467f82b-34be-4d10-816c-b3e4231c92a1">OLEUIPASTEFLAG</a>



<a href="https://msdn.microsoft.com/bb346fa7-03ae-458d-8488-64db7a9c48e1">OLEUIPASTESPECIAL</a>



<a href="https://msdn.microsoft.com/fb1335da-a863-4d15-8a8d-289d8cccd13f">OleUIPasteSpecial</a>
 

 

