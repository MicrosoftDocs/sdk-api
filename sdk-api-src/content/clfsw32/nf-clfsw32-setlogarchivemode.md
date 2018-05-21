---
UID: NF:clfsw32.SetLogArchiveMode
title: SetLogArchiveMode function
author: windows-driver-content
description: Enables or disables log archive support for a specified log.
old-location: fs\setlogarchivemode.htm
old-project: Clfs
ms.assetid: 9f8a9ab9-2873-44c2-aa8d-78514ffe42bb
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: CLFS_LOG_ARCHIVE_MODE, ClfsLogArchiveDisabled, ClfsLogArchiveEnabled, SetLogArchiveMode, SetLogArchiveMode function [Files], clfsw32/SetLogArchiveMode, fs.setlogarchivemode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: clfsw32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: LOG_MANAGEMENT_CALLBACKS, *PLOG_MANAGEMENT_CALLBACKS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	ClfsW32.dll
api_name:
-	SetLogArchiveMode
product: Windows
targetos: Windows
req.lib: ClfsW32.lib
req.dll: ClfsW32.dll
req.irql: 
---

# SetLogArchiveMode function


## -description


Enables or disables log archive support for a specified log.


## -parameters




### -param hLog [in]

A handle to the log that is obtained from 
      <a href="https://msdn.microsoft.com/ac104bf9-7ca7-417a-bd14-09b0e82c6a77">CreateLogFile</a>.


### -param eMode [in]


Specifies whether to make the log ephemeral. This parameter can be one of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ClfsLogArchiveEnabled"></a><a id="clfslogarchiveenabled"></a><a id="CLFSLOGARCHIVEENABLED"></a><dl>
<dt><b>ClfsLogArchiveEnabled</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Enable log archive (ephemeral logs) support.

</td>
</tr>
<tr>
<td width="40%"><a id="ClfsLogArchiveDisabled"></a><a id="clfslogarchivedisabled"></a><a id="CLFSLOGARCHIVEDISABLED"></a><dl>
<dt><b>ClfsLogArchiveDisabled</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Disables ephemeral logs.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value is nonzero.
      

If the function fails, the return value is zero (0). To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/a3059828-d291-493d-a4fe-13d06e49ed12">Common Log File System Functions</a>
 

 

