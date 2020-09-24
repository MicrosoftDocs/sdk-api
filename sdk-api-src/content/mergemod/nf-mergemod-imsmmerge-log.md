---
UID: NF:mergemod.IMsmMerge.Log
title: IMsmMerge::Log (mergemod.h)
description: The Log method writes a text string to the currently open log file. For more information, see the Log method of the Merge object.
helpviewer_keywords: ["IMsmMerge interface","Log method","IMsmMerge.Log","IMsmMerge::Log","Log","Log method","Log method","IMsmMerge interface","_msi_log_function","mergemod/IMsmMerge::Log","setup.imsmmerge_log"]
old-location: setup\imsmmerge_log.htm
tech.root: setup
ms.assetid: 15c7450b-6887-4a54-8f4f-ac2cf5944f17
ms.date: 12/05/2018
ms.keywords: IMsmMerge interface,Log method, IMsmMerge.Log, IMsmMerge::Log, Log, Log method, Log method,IMsmMerge interface, _msi_log_function, mergemod/IMsmMerge::Log, setup.imsmmerge_log
req.header: mergemod.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Mergemod.dll 1.0 or later
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
req.dll: Mergemod.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMsmMerge::Log
 - mergemod/IMsmMerge::Log
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mergemod.dll
api_name:
 - IMsmMerge.Log
---

# IMsmMerge::Log


## -description

The 
<b>Log</b> method writes a text string to the currently open log file. For more information, see the 
<a href="/windows/desktop/Msi/merge-log">Log</a> method of the 
<a href="/windows/desktop/Msi/merge-object">Merge</a> object. 

<b>IMsmMerge2::Log</b>    Mergemod.dll version 2.0 or later.
			<div> </div><b>IMsmMerge::Log</b>      All Mergemod.dll versions.

## -parameters

### -param Message

The text string to display. A <b>LPCWSTR</b> may be used instead of a <b>BSTR</b>.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
There was an error writing to the log file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The argument is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No log file is open.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/Msi/merge-module-automation">Merge Module Automation</a>