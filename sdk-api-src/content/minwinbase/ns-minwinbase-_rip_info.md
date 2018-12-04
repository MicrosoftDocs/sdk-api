---
UID: NS:minwinbase._RIP_INFO
title: "_RIP_INFO"
author: windows-sdk-content
description: Contains the error that caused the RIP debug event.
old-location: base\rip_info_str.htm
tech.root: debug
ms.assetid: 2aef4de7-bf3d-4add-9801-e26081f0f76b
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: "*LPRIP_INFO, LPRIP_INFO, LPRIP_INFO structure pointer, RIP_INFO, RIP_INFO structure, SLE_ERROR, SLE_MINORERROR, SLE_WARNING, _RIP_INFO, _win32_rip_info_str, base.rip_info_str, winbase/LPRIP_INFO, winbase/RIP_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: minwinbase.h
req.include-header: Minwinbase.h, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - WinBase.h
api_name:
 - RIP_INFO
product: Windows
targetos: Windows
req.typenames: RIP_INFO, *LPRIP_INFO
req.redist: 
---

# _RIP_INFO structure


## -description


Contains the error that caused the RIP debug event.


## -struct-fields




### -field dwError

The error that caused the RIP debug event. For more information, see 
<a href="https://msdn.microsoft.com/b8d84980-6ba9-4784-8ab0-d5e9c5c95bae">Error Handling</a>.


### -field dwType

Any additional information about the type of error that caused the RIP debug event. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SLE_ERROR"></a><a id="sle_error"></a><dl>
<dt><b>SLE_ERROR</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Indicates that invalid data was passed to the function that failed. This caused the application to fail.

</td>
</tr>
<tr>
<td width="40%"><a id="SLE_MINORERROR"></a><a id="sle_minorerror"></a><dl>
<dt><b>SLE_MINORERROR</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Indicates that invalid data was passed to the function, but the error probably will not cause the application to fail.

</td>
</tr>
<tr>
<td width="40%"><a id="SLE_WARNING"></a><a id="sle_warning"></a><dl>
<dt><b>SLE_WARNING</b></dt>
<dt>0x00000003</dt>
</dl>
</td>
<td width="60%">
Indicates that potentially invalid data was passed to the function, but the function completed processing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Indicates that only <b>dwError</b> was set.

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/056aa7ee-51ca-48ec-9cd7-26085bb85b11">DEBUG_EVENT</a>
 

 

