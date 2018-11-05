---
UID: NF:winddi.DrvLoadFontFile
title: DrvLoadFontFile function
author: windows-sdk-content
description: The DrvLoadFontFile function receives information from GDI relating to loading and mapping font files.
old-location: display\drvloadfontfile.htm
tech.root: display
ms.assetid: d9bcf8f8-40bc-48dc-85b7-67773c8a4ded
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: DrvLoadFontFile, DrvLoadFontFile function [Display Devices], ddifncs_42238b28-ad71-4df8-b572-4ffd7ca2d3c1.xml, display.drvloadfontfile, winddi/DrvLoadFontFile
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - winddi.h
api_name:
 - DrvLoadFontFile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DrvLoadFontFile function


## -description


The <b>DrvLoadFontFile</b> function receives information from GDI relating to loading and mapping font files.


## -parameters




### -param cFiles

Caller-supplied value indicating the number of files associated with the font.


### -param piFile

Caller-supplied pointer to a <i>cFiles</i>-sized array of file handles. Each handle represents one of the files associated with the font. The file handles can be passed individually to <a href="https://msdn.microsoft.com/582570b0-981f-4852-974f-cb6575c68717">EngMapFontFileFD</a>.


### -param ppvView

Caller-supplied pointer to a <i>cFiles</i>-sized array containing the starting address of the memory space into which each font file has been mapped.


### -param pcjView

Caller-supplied pointer to a <i>cFiles</i>-sized array containing the size of the memory space into which each font file has been mapped.


### -param pdv

For Adobe Multiple Master fonts, this is a caller-supplied pointer to a DESIGNVECTOR structure (described in the Microsoft Windows SDK documentation) identifying the Multiple Master instance. Otherwise, this parameter is <b>NULL</b>.


### -param ulLangID

Caller-supplied language identifier, obtained from the registry.


### -param ulFastCheckSum

Specifies a GDI-supplied checksum for the font. If this parameter is nonzero, the GDI font cache engine can be used in order to access a font more quickly. If this parameter is zero, the GDI font engine cannot be used. 


## -returns



If the operation succeeds, it should return a pointer to a driver-defined value that uniquely identifies the font. The driver subsequently receives this pointer as an input parameter to such functions as <a href="https://msdn.microsoft.com/2ba6c8e3-9707-48dd-98d9-072f3eee8cd0">DrvQueryFont</a>, <a href="https://msdn.microsoft.com/4d853dbd-0448-43c3-9f01-13b7118a0743">DrvQueryFontFile</a>, <a href="https://msdn.microsoft.com/29601ea6-9b68-4cdc-a7a1-b6a922524760">DrvQueryFontTree</a>. If an error is encountered, the function should return HFF_INVALID.




## -remarks



Font drivers are required to supply a <b>DrvLoadFontFile</b> function. The function's purpose is to allow a font driver to receive notification that a font's associated files are being loaded and mapped. The driver can store input arguments for later use.

Loading and mapping a font file entails calling <a href="https://msdn.microsoft.com/582570b0-981f-4852-974f-cb6575c68717">EngMapFontFileFD</a>. When an application calls <b>AddFontResource</b> or AddFontResourceEx (described in the Windows SDK documentation), GDI calls <b>EngMapFontFileFD</b> and then calls <b>DrvLoadFontFile</b>. The <b>DrvLoadFontFile</b> function's <i>ppvView</i> and <i>pcjView</i> parameters supply the location and size of each file's mapping, as returned by <b>EngMapFontFileFD</b>.

GDI unmaps the files when <b>DrvLoadFontFile</b> returns. If the driver needs to remap the files later, in response to subsequent calls from GDI, it can call <a href="https://msdn.microsoft.com/582570b0-981f-4852-974f-cb6575c68717">EngMapFontFileFD</a> itself if it has saved the <i>cFiles</i> and <i>piFile</i> parameters.

When the GDI font engine calls the font driver's <b>DrvLoadFontFile</b> DDI, it passes a checksum for the font in the <i>ulFastCheckSum</i>  parameter. If this parameter is nonzero and the font in question has been cached, <b>DrvLoadFontFile</b> can obtain a pointer to the font data with a call to <a href="https://msdn.microsoft.com/daf93826-fdcb-4c9d-ade6-ad4f0ef40ff5">EngFntCacheLookUp</a>. After the font driver obtains the pointer to the font data, it can then load the font data. If the font has not been cached, the font driver can cache the font by first allocating memory for the font cache, using a call to <a href="https://msdn.microsoft.com/fd0765e0-decd-46fb-872e-4c750713abe6">EngFntCacheAlloc</a>, and then writing the font data to that memory. If the font driver encounters an error reading or writing the font data, it can notify the GDI font engine by making a call to <a href="https://msdn.microsoft.com/27a44779-64df-4a3f-b8b8-9e0417010969">EngFntCacheFault</a>.

If the GDI font engine called <b>DrvLoadFontFile</b> and passed in a value of zero for the <i>ulFastCheckSum</i> parameter, this means that the GDI font engine is not in operation, and the font driver does not need to take any action.




## -see-also




<a href="https://msdn.microsoft.com/2b4b946a-30d0-434f-ab04-73bedd6a01aa">DrvUnloadFontFile</a>



<a href="https://msdn.microsoft.com/fd0765e0-decd-46fb-872e-4c750713abe6">EngFntCacheAlloc</a>



<a href="https://msdn.microsoft.com/27a44779-64df-4a3f-b8b8-9e0417010969">EngFntCacheFault</a>



<a href="https://msdn.microsoft.com/daf93826-fdcb-4c9d-ade6-ad4f0ef40ff5">EngFntCacheLookUp</a>
 

 

