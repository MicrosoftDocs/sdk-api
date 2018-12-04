---
UID: NF:winddi.EngFntCacheFault
title: EngFntCacheFault function
author: windows-sdk-content
description: The EngFntCacheFault function reports an error to the font engine if the font driver encountered an error reading from or writing to a font data cache.
old-location: display\engfntcachefault.htm
tech.root: display
ms.assetid: 27a44779-64df-4a3f-b8b8-9e0417010969
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: EngFntCacheFault, EngFntCacheFault function [Display Devices], display.engfntcachefault, gdifncs_f6395707-6ff6-4396-b280-77d4256db07b.xml, winddi/EngFntCacheFault
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: This function is available in Windows XP and later.
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
 - EngFntCacheFault
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EngFntCacheFault function


## -description


The <b>EngFntCacheFault</b> function reports an error to the font engine if the font driver encountered an error reading from or writing to a font data cache.


## -parameters




### -param ulFastCheckSum [in]

Specifies the checksum for the font.


### -param iFaultMode [in]

Specifies the type of error that occurred. This parameter can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
ENG_FNT_CACHE_READ_FAULT

</td>
<td>
An error occurred during retrieval.

</td>
</tr>
<tr>
<td>
ENG_FNT_CACHE_WRITE_FAULT

</td>
<td>
An error occurred during storage.

</td>
</tr>
</table>
 


## -returns



None




## -remarks



If an error occurs while the font driver was reading from or writing to the font data cache, it should report the error to the font engine by a call to this function.

The font engine calls the font driver's <a href="https://msdn.microsoft.com/d9bcf8f8-40bc-48dc-85b7-67773c8a4ded">DrvLoadFontFile</a> entry point when a font file is first loaded. It is in this call that the font driver receives a value for <i>ulFastCheckSum</i>, which it subsequently uses when it calls this function.




## -see-also




<a href="https://msdn.microsoft.com/d9bcf8f8-40bc-48dc-85b7-67773c8a4ded">DrvLoadFontFile</a>



<a href="https://msdn.microsoft.com/fd0765e0-decd-46fb-872e-4c750713abe6">EngFntCacheAlloc</a>



<a href="https://msdn.microsoft.com/daf93826-fdcb-4c9d-ade6-ad4f0ef40ff5">EngFntCacheLookUp</a>
 

 

