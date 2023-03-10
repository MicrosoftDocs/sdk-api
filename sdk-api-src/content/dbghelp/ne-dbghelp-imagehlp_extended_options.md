---
UID: NE:dbghelp.IMAGEHLP_EXTENDED_OPTIONS
title: IMAGEHLP_EXTENDED_OPTIONS (dbghelp.h)
description: Lists the extended symbol options that you can get and set by using the SymGetExtendedOption and SymSetExtendedOption functions.
helpviewer_keywords: ["IMAGEHLP_EXTENDED_OPTIONS","IMAGEHLP_EXTENDED_OPTIONS enumeration","SYMOPT_EX_DISABLEACCESSTIMEUPDATE","SYMOPT_EX_MAX","base.imagehlp_extended_options","dbghelp/IMAGEHLP_EXTENDED_OPTIONS","dbghelp/SYMOPT_EX_DISABLEACCESSTIMEUPDATE","dbghelp/SYMOPT_EX_MAX"]
old-location: base\imagehlp_extended_options.htm
tech.root: Debug
ms.assetid: 5354F53C-F161-4887-85E4-7A00521034EE
ms.date: 12/05/2018
ms.keywords: IMAGEHLP_EXTENDED_OPTIONS, IMAGEHLP_EXTENDED_OPTIONS enumeration, SYMOPT_EX_DISABLEACCESSTIMEUPDATE, SYMOPT_EX_MAX, base.imagehlp_extended_options, dbghelp/IMAGEHLP_EXTENDED_OPTIONS, dbghelp/SYMOPT_EX_DISABLEACCESSTIMEUPDATE, dbghelp/SYMOPT_EX_MAX
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
targetos: Windows
req.typenames: IMAGEHLP_EXTENDED_OPTIONS
req.redist: DbgHelp.dll 10.0.16232.1000 or later
ms.custom: 19H1
f1_keywords:
 - IMAGEHLP_EXTENDED_OPTIONS
 - dbghelp/IMAGEHLP_EXTENDED_OPTIONS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DbgHelp.h
api_name:
 - IMAGEHLP_EXTENDED_OPTIONS
---

# IMAGEHLP_EXTENDED_OPTIONS enumeration


## -description

Lists the extended symbol options that you can get and set by using the <a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgetextendedoption">SymGetExtendedOption</a> and <a href="/windows/desktop/api/dbghelp/nf-dbghelp-symsetextendedoption">SymSetExtendedOption</a> functions.

## -enum-fields

### -field SYMOPT_EX_DISABLEACCESSTIMEUPDATE

Turns off explicit updates to the last access time of a symbol that is loaded. By default, DbgHelp updates the last access time of a symbol file that is consumed so that a symbol cache can be maintained by using a least recently used mechanism.

### -field SYMOPT_EX_MAX

Unused.

## -see-also

<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgetextendedoption">SymGetExtendedOption</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symsetextendedoption">SymSetExtendedOption</a>

