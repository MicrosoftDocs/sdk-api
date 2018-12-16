---
UID: NS:dbghelp._IMAGEHLP_CBA_EVENTW
title: IMAGEHLP_CBA_EVENTW
author: windows-sdk-content
description: Contains information about a debugging event.
old-location: base\imagehlp_cba_event_str.htm
tech.root: debug
ms.assetid: 1d63007a-7542-4626-99a5-41461e00dbb4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PIMAGEHLP_CBA_EVENTW, IMAGEHLP_CBA_EVENT, IMAGEHLP_CBA_EVENT structure, IMAGEHLP_CBA_EVENTW, PIMAGEHLP_CBA_EVENT, PIMAGEHLP_CBA_EVENT structure pointer, _IMAGEHLP_CBA_EVENT, _IMAGEHLP_CBA_EVENTW, base.imagehlp_cba_event_str, dbghelp/IMAGEHLP_CBA_EVENT, dbghelp/IMAGEHLP_CBA_EVENTW, dbghelp/PIMAGEHLP_CBA_EVENT, sevAttn, sevFatal, sevInfo, sevProblem"
ms.topic: struct
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: IMAGEHLP_CBA_EVENTW (Unicode) and IMAGEHLP_CBA_EVENT (ANSI)
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
 - IMAGEHLP_CBA_EVENT
 - IMAGEHLP_CBA_EVENT
 - IMAGEHLP_CBA_EVENTW
product: Windows
targetos: Windows
req.typenames: IMAGEHLP_CBA_EVENTW, *PIMAGEHLP_CBA_EVENTW
req.redist: DbgHelp.dll 6.1 or later
---

# IMAGEHLP_CBA_EVENTW structure


## -description


Contains information about a debugging event.


## -struct-fields




### -field severity

The event severity. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="sevInfo"></a><a id="sevinfo"></a><a id="SEVINFO"></a><dl>
<dt><b>sevInfo</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Informational event.

</td>
</tr>
<tr>
<td width="40%"><a id="sevProblem"></a><a id="sevproblem"></a><a id="SEVPROBLEM"></a><dl>
<dt><b>sevProblem</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Reserved for future use.

</td>
</tr>
<tr>
<td width="40%"><a id="sevAttn"></a><a id="sevattn"></a><a id="SEVATTN"></a><dl>
<dt><b>sevAttn</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Reserved for future use.

</td>
</tr>
<tr>
<td width="40%"><a id="sevFatal"></a><a id="sevfatal"></a><a id="SEVFATAL"></a><dl>
<dt><b>sevFatal</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Reserved for future use.

</td>
</tr>
</table>
 


### -field code

This member is reserved for future use.


### -field desc

A text description of the error.


### -field object

This member is reserved for future use.


## -see-also




<a href="https://msdn.microsoft.com/f3ba952b-ecc5-4235-a806-00c82d40e611">SymRegisterCallbackProc64</a>



<a href="base.symbolservercallback">SymbolServerCallback</a>
 

 

