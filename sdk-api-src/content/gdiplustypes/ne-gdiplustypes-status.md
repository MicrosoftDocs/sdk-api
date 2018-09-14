---
UID: NE:gdiplustypes.Status
title: Status
author: windows-sdk-content
description: The Status enumeration indicates the result of a Windows GDI+ method call.
old-location: gdiplus\_gdiplus_ENUM_Status.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\status.htm
ms.author: windowssdkdev
ms.date: 09/12/2018
ms.keywords: Aborted, AccessDenied, FileNotFound, FontFamilyNotFound, FontStyleNotFound, GdiplusNotInitialized, GenericError, InsufficientBuffer, InvalidParameter, NotImplemented, NotTrueTypeFont, ObjectBusy, Ok, OutOfMemory, ProfileNotFound, PropertyNotFound, PropertyNotSupported, Status, Status enumeration [GDI+], UnknownImageFormat, UnsupportedGdiplusVersion, ValueOverflow, Win32Error, WrongState, _gdiplus_ENUM_Status, gdiplus._gdiplus_ENUM_Status, gdiplustypes/Aborted, gdiplustypes/AccessDenied, gdiplustypes/FileNotFound, gdiplustypes/FontFamilyNotFound, gdiplustypes/FontStyleNotFound, gdiplustypes/GdiplusNotInitialized, gdiplustypes/GenericError, gdiplustypes/InsufficientBuffer, gdiplustypes/InvalidParameter, gdiplustypes/NotImplemented, gdiplustypes/NotTrueTypeFont, gdiplustypes/ObjectBusy, gdiplustypes/Ok, gdiplustypes/OutOfMemory, gdiplustypes/ProfileNotFound, gdiplustypes/PropertyNotFound, gdiplustypes/PropertyNotSupported, gdiplustypes/Status, gdiplustypes/UnknownImageFormat, gdiplustypes/UnsupportedGdiplusVersion, gdiplustypes/ValueOverflow, gdiplustypes/Win32Error, gdiplustypes/WrongState
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Gdiplustypes.h
api_name:
 - Status
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.1
---

# Status enumeration


## -description


The <b>Status</b> enumeration indicates the result of a Windows GDI+ method call.


## -enum-fields




### -field Ok

Indicates that the method call was successful. 


### -field GenericError

Indicates that there was an error on the method call, which is identified as something other than those defined by the other elements of this enumeration. 


### -field InvalidParameter

Indicates that one of the arguments passed to the method was not valid. 


### -field OutOfMemory

Indicates that the operating system is out of memory and could not allocate memory to process the method call. For an explanation of how constructors use the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">OutOfMemory</a> status, see the Remarks section at the end of this topic. 


### -field ObjectBusy

Indicates that one of the arguments specified in the API call is already in use in another thread. 


### -field InsufficientBuffer

Indicates that a buffer specified as an argument in the API call is not large enough to hold the data to be received. 


### -field NotImplemented

Indicates that the method is not implemented. 


### -field Win32Error

Indicates that the method generated a Win32 error. 


### -field WrongState

Indicates that the object is in an invalid state to satisfy the API call. For example, calling 
				<a href="https://msdn.microsoft.com/4121c28f-0402-46fa-9501-0e41de21bae5">Pen::GetColor</a> from a pen that is not a single, solid color results in a <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">WrongState</a> status. 


### -field Aborted

Indicates that the method was aborted. 


### -field FileNotFound

Indicates that the specified image file or metafile cannot be found. 


### -field ValueOverflow

Indicates that the method performed an arithmetic operation that produced a numeric overflow. 


### -field AccessDenied

Indicates that a write operation is not allowed on the specified file. 


### -field UnknownImageFormat

Indicates that the specified image file format is not known. 


### -field FontFamilyNotFound

Indicates that the specified font family cannot be found. Either the font family name is incorrect or the font family is not installed. 


### -field FontStyleNotFound

Indicates that the specified style is not available for the specified font family. 


### -field NotTrueTypeFont

Indicates that the font retrieved from an 
				<b>HDC</b> or 
				<b>LOGFONT</b> is not a TrueType font and cannot be used with GDI+. 


### -field UnsupportedGdiplusVersion

Indicates that the version of GDI+ that is installed on the system is incompatible with the version with which the application was compiled. 


### -field GdiplusNotInitialized

Indicates that the GDI+API is not in an initialized state. To function, all GDI+ objects require that GDI+ be in an initialized state. Initialize GDI+ by calling 
				<a href="https://msdn.microsoft.com/3748a252-db65-4471-8345-ab0c136c5a21">GdiplusStartup</a>. 


### -field PropertyNotFound

Indicates that the specified property does not exist in the image. 


### -field PropertyNotSupported

Indicates that the specified property is not supported by the format of the image and, therefore, cannot be set. 


### -field ProfileNotFound

Indicates that the color profile required to save an image in CMYK format was not found.


## -remarks



If you construct a GDI+ object and then immediately call the 
				<b>GetLastStatus</b> method of that object, you can determine whether the constructor succeeded or failed. In such cases, 
				<b>GetLastStatus</b> might return <b><b>OutOfMemory</b></b> even though there was plenty of memory available to create the object. Several GDI+ constructors set the status to <b><b>OutOfMemory</b></b> when they fail regardless of the reason for failure.



