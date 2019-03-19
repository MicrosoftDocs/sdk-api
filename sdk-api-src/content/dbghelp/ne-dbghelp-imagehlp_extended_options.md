---
UID: NE:dbghelp.__unnamed_enum_4
title: IMAGEHLP_EXTENDED_OPTIONS (dbghelp.h)
author: windows-sdk-content
description: Lists the extended symbol options that you can get and set by using the SymGetExtendedOption and SymSetExtendedOption functions.
old-location: base\imagehlp_extended_options.htm
tech.root: Debug
ms.assetid: 5354F53C-F161-4887-85E4-7A00521034EE
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMAGEHLP_EXTENDED_OPTIONS, IMAGEHLP_EXTENDED_OPTIONS enumeration, SYMOPT_EX_DISABLEACCESSTIMEUPDATE, SYMOPT_EX_MAX, base.imagehlp_extended_options, dbghelp/IMAGEHLP_EXTENDED_OPTIONS, dbghelp/SYMOPT_EX_DISABLEACCESSTIMEUPDATE, dbghelp/SYMOPT_EX_MAX
ms.topic: enum
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
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
 - DbgHelp.h
api_name:
 - IMAGEHLP_EXTENDED_OPTIONS
product: Windows
targetos: Windows
req.typenames: IMAGEHLP_EXTENDED_OPTIONS
req.redist: DbgHelp.dll 10.0.16232.1000 or later
---

# IMAGEHLP_EXTENDED_OPTIONS enumeration


## -description


Lists the extended symbol options that you can get and set by using the <a href="https://msdn.microsoft.com/3D6D5E31-ECCB-48B2-A46B-0BB2D7A2DEC0">SymGetExtendedOption</a> and <a href="https://msdn.microsoft.com/25756250-D2B4-4D5A-BED0-238C34C18093">SymSetExtendedOption</a> functions.


## -enum-fields




### -field SYMOPT_EX_DISABLEACCESSTIMEUPDATE

Turns off explicit updates to the last access time of a symbol that is loaded. By default, DbgHelp updates the last access time of a symbol file that is consumed so that a symbol cache can be maintained by using a least recently used mechanism.


### -field SYMOPT_EX_MAX

Unused.


## -see-also




<a href="https://msdn.microsoft.com/3D6D5E31-ECCB-48B2-A46B-0BB2D7A2DEC0">SymGetExtendedOption</a>



<a href="https://msdn.microsoft.com/25756250-D2B4-4D5A-BED0-238C34C18093">SymSetExtendedOption</a>
 

 

