---
UID: NS:wingdi.tagCHARSETINFO
title: CHARSETINFO (wingdi.h)
author: windows-sdk-content
description: Contains information about a character set.
old-location: intl\charsetinfo.htm
tech.root: Intl
ms.assetid: 4f815f53-9fac-41f3-9493-bd8d68cff543
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPCHARSETINFO, *NPCHARSETINFO, *PCHARSETINFO, CHARSETINFO, CHARSETINFO structure [Internationalization for Windows Applications], PCHARSETINFO, PCHARSETINFO structure pointer [Internationalization for Windows Applications], _win32_CHARSETINFO_str, intl.charsetinfo, wingdi/CHARSETINFO, wingdi/PCHARSETINFO"
ms.topic: struct
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Wingdi.h
api_name:
 - CHARSETINFO
product: Windows
targetos: Windows
req.typenames: CHARSETINFO, *PCHARSETINFO, *NPCHARSETINFO, *LPCHARSETINFO
req.redist: 
---

# CHARSETINFO structure


## -description



Contains information about a character set.




## -struct-fields




### -field ciCharset

Character set value.


### -field ciACP

Windows ANSI code page identifier. For a list of identifiers, see <a href="https://msdn.microsoft.com/5d6fc86a-f205-4d14-bb7c-ecd71682e0fe">Code Page Identifiers</a>.


### -field fs

A <a href="https://msdn.microsoft.com/5331da53-7e3d-46e9-a922-da04fedc8382">FONTSIGNATURE</a> structure that identifies the Unicode subrange and the specific Windows ANSI character set/code page. Only one code page will be set when this structure is set by the function.


## -see-also




<a href="https://msdn.microsoft.com/866f09f4-629e-4097-a974-fbda9389d077">Code Pages</a>



<a href="https://msdn.microsoft.com/5331da53-7e3d-46e9-a922-da04fedc8382">FONTSIGNATURE</a>



<a href="https://msdn.microsoft.com/0e6e81f1-ec7b-42ba-8706-a352349fa6ab">TranslateCharsetInfo</a>



<a href="https://msdn.microsoft.com/0c8120dd-3270-4343-8b0c-b91ff555f276">Unicode and Character Set Structures</a>
 

 

