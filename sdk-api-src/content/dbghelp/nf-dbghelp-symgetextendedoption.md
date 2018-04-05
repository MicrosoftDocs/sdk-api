---
UID: NF:dbghelp.SymGetExtendedOption
title: SymGetExtendedOption function
author: windows-driver-content
description: Gets whether the specified extended symbol option on or off.
old-location: base\symgetextendedoption.htm
old-project: Debug
ms.assetid: 3D6D5E31-ECCB-48B2-A46B-0BB2D7A2DEC0
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: SYMOPT_EX_DISABLEACCESSTIMEUPDATE, SymGetExtendedOption, SymGetExtendedOption function, base.symgetextendedoption, dbghelp/SymGetExtendedOption
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: IMAGEHLP_SYMBOL_TYPE_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	DbgHelp.dll
-	ImageHlp.dll
api_name:
-	SymGetExtendedOption
product: Windows
targetos: Windows
req.lib: DbgHelp.lib
req.dll: DbgHelp.dll
req.irql: 
---

# SymGetExtendedOption function


## -description


Gets whether the specified extended symbol option on or off.


## -parameters




### -param option [in]

The extended symbol option to check. The following are valid values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SYMOPT_EX_DISABLEACCESSTIMEUPDATE"></a><a id="symopt_ex_disableaccesstimeupdate"></a><dl>
<dt><b>SYMOPT_EX_DISABLEACCESSTIMEUPDATE</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Turns off explicit updates to the last access time of a symbol that is loaded. By default, DbgHelp updates the last access time of a symbol file that is consumed so that a symbol cache can be maintained by using a least recently used mechanism.

</td>
</tr>
</table>
 


## -returns



The value of the specified symbol option.




## -see-also




<a href="https://msdn.microsoft.com/5354F53C-F161-4887-85E4-7A00521034EE">IMAGEHLP_EXTENDED_OPTIONS</a>



<a href="https://msdn.microsoft.com/25756250-D2B4-4D5A-BED0-238C34C18093">SymSetExtendedOption</a>
 

 

