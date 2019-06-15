---
UID: NF:winddi.EngUnmapFontFileFD
title: EngUnmapFontFileFD function (winddi.h)
author: windows-sdk-content
description: The EngUnmapFontFileFD function unmaps the specified font file from system memory.
old-location: display\engunmapfontfilefd.htm
tech.root: display
ms.assetid: 61c1acb6-c158-4ba4-ad5b-2f7b1a9bf106
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EngUnmapFontFileFD, EngUnmapFontFileFD function [Display Devices], display.engunmapfontfilefd, gdifncs_40ba83d0-7822-402b-9463-f593ddaecaed.xml, winddi/EngUnmapFontFileFD
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
api_name:
 - EngUnmapFontFileFD
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EngUnmapFontFileFD function


## -description


The <b>EngUnmapFontFileFD</b> function unmaps the specified font file from system memory.


## -parameters




### -param iFile [in]

Pointer to a driver-defined value that identifies the font file to be unmapped. This pointer is obtained from <a href="https://docs.microsoft.com/windows/desktop/api/winddi/nf-winddi-drvloadfontfile">DrvLoadFontFile</a>.


## -returns



None




## -remarks



A font driver calls <b>EngUnmapFontFileFD</b> to unmap a font file that was previously mapped by <a href="https://docs.microsoft.com/windows/desktop/api/winddi/nf-winddi-engmapfontfilefd">EngMapFontFileFD</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winddi/nf-winddi-drvloadfontfile">DrvLoadFontFile</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winddi/nf-winddi-engmapfontfilefd">EngMapFontFileFD</a>
 

 

