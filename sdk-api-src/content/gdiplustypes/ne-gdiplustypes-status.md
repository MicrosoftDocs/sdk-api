---
UID: NE:gdiplustypes.Status
title: Status (gdiplustypes.h)
description: The Status enumeration indicates the result of a Windows GDI+ method call.
helpviewer_keywords: ["Aborted","AccessDenied","FileNotFound","FontFamilyNotFound","FontStyleNotFound","GdiplusNotInitialized","GenericError","InsufficientBuffer","InvalidParameter","NotImplemented","NotTrueTypeFont","ObjectBusy","Ok","OutOfMemory","ProfileNotFound","PropertyNotFound","PropertyNotSupported","Status","Status enumeration [GDI+]","UnknownImageFormat","UnsupportedGdiplusVersion","ValueOverflow","Win32Error","WrongState","_gdiplus_ENUM_Status","gdiplus._gdiplus_ENUM_Status","gdiplustypes/Aborted","gdiplustypes/AccessDenied","gdiplustypes/FileNotFound","gdiplustypes/FontFamilyNotFound","gdiplustypes/FontStyleNotFound","gdiplustypes/GdiplusNotInitialized","gdiplustypes/GenericError","gdiplustypes/InsufficientBuffer","gdiplustypes/InvalidParameter","gdiplustypes/NotImplemented","gdiplustypes/NotTrueTypeFont","gdiplustypes/ObjectBusy","gdiplustypes/Ok","gdiplustypes/OutOfMemory","gdiplustypes/ProfileNotFound","gdiplustypes/PropertyNotFound","gdiplustypes/PropertyNotSupported","gdiplustypes/Status","gdiplustypes/UnknownImageFormat","gdiplustypes/UnsupportedGdiplusVersion","gdiplustypes/ValueOverflow","gdiplustypes/Win32Error","gdiplustypes/WrongState"]
old-location: gdiplus\_gdiplus_ENUM_Status.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\status.htm
ms.date: 12/05/2018
ms.keywords: Aborted, AccessDenied, FileNotFound, FontFamilyNotFound, FontStyleNotFound, GdiplusNotInitialized, GenericError, InsufficientBuffer, InvalidParameter, NotImplemented, NotTrueTypeFont, ObjectBusy, Ok, OutOfMemory, ProfileNotFound, PropertyNotFound, PropertyNotSupported, Status, Status enumeration [GDI+], UnknownImageFormat, UnsupportedGdiplusVersion, ValueOverflow, Win32Error, WrongState, _gdiplus_ENUM_Status, gdiplus._gdiplus_ENUM_Status, gdiplustypes/Aborted, gdiplustypes/AccessDenied, gdiplustypes/FileNotFound, gdiplustypes/FontFamilyNotFound, gdiplustypes/FontStyleNotFound, gdiplustypes/GdiplusNotInitialized, gdiplustypes/GenericError, gdiplustypes/InsufficientBuffer, gdiplustypes/InvalidParameter, gdiplustypes/NotImplemented, gdiplustypes/NotTrueTypeFont, gdiplustypes/ObjectBusy, gdiplustypes/Ok, gdiplustypes/OutOfMemory, gdiplustypes/ProfileNotFound, gdiplustypes/PropertyNotFound, gdiplustypes/PropertyNotSupported, gdiplustypes/Status, gdiplustypes/UnknownImageFormat, gdiplustypes/UnsupportedGdiplusVersion, gdiplustypes/ValueOverflow, gdiplustypes/Win32Error, gdiplustypes/WrongState
req.header: gdiplustypes.h
req.include-header: Gdiplus.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.1
ms.custom: 19H1
f1_keywords:
 - Status
 - gdiplustypes/Status
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Gdiplustypes.h
api_name:
 - Status
---

# Status enumeration


## -description

The <b>Status</b> enumeration indicates the result of a Windows GDI+ method call.

## -enum-fields

### -field Ok:0

Indicates that the method call was successful.

### -field GenericError:1

Indicates that there was an error on the method call, which is identified as something other than those defined by the other elements of this enumeration.

### -field InvalidParameter:2

Indicates that one of the arguments passed to the method was not valid.

### -field OutOfMemory:3

Indicates that the operating system is out of memory and could not allocate memory to process the method call. For an explanation of how constructors use the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">OutOfMemory</a> status, see the Remarks section at the end of this topic.

### -field ObjectBusy:4

Indicates that one of the arguments specified in the API call is already in use in another thread.

### -field InsufficientBuffer:5

Indicates that a buffer specified as an argument in the API call is not large enough to hold the data to be received.

### -field NotImplemented:6

Indicates that the method is not implemented.

### -field Win32Error:7

Indicates that the method generated a Win32 error.

### -field WrongState:8

Indicates that the object is in an invalid state to satisfy the API call. For example, calling 
				<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-getcolor">Pen::GetColor</a> from a pen that is not a single, solid color results in a <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">WrongState</a> status.

### -field Aborted:9

Indicates that the method was aborted.

### -field FileNotFound:10

Indicates that the specified image file or metafile cannot be found.

### -field ValueOverflow:11

Indicates that the method performed an arithmetic operation that produced a numeric overflow.

### -field AccessDenied:12

Indicates that a write operation is not allowed on the specified file.

### -field UnknownImageFormat:13

Indicates that the specified image file format is not known.

### -field FontFamilyNotFound:14

Indicates that the specified font family cannot be found. Either the font family name is incorrect or the font family is not installed.

### -field FontStyleNotFound:15

Indicates that the specified style is not available for the specified font family.

### -field NotTrueTypeFont:16

Indicates that the font retrieved from an 
				<b>HDC</b> or 
				<b>LOGFONT</b> is not a TrueType font and cannot be used with GDI+.

### -field UnsupportedGdiplusVersion:17

Indicates that the version of GDI+ that is installed on the system is incompatible with the version with which the application was compiled.

### -field GdiplusNotInitialized:18

Indicates that the GDI+API is not in an initialized state. To function, all GDI+ objects require that GDI+ be in an initialized state. Initialize GDI+ by calling 
				<a href="/windows/desktop/api/gdiplusinit/nf-gdiplusinit-gdiplusstartup">GdiplusStartup</a>.

### -field PropertyNotFound:19

Indicates that the specified property does not exist in the image.

### -field PropertyNotSupported:20

Indicates that the specified property is not supported by the format of the image and, therefore, cannot be set.

### -field ProfileNotFound:21

Indicates that the color profile required to save an image in CMYK format was not found.

## -remarks

If you construct a GDI+ object and then immediately call the 
				<b>GetLastStatus</b> method of that object, you can determine whether the constructor succeeded or failed. In such cases, 
				<b>GetLastStatus</b> might return <b><b>OutOfMemory</b></b> even though there was plenty of memory available to create the object. Several GDI+ constructors set the status to <b><b>OutOfMemory</b></b> when they fail regardless of the reason for failure.
