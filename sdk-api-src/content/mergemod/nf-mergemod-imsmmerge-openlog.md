---
UID: NF:mergemod.IMsmMerge.OpenLog
title: IMsmMerge::OpenLog (mergemod.h)
description: The OpenLog method opens a log file that receives progress and error messages.
helpviewer_keywords: ["IMsmMerge interface","OpenLog method","IMsmMerge.OpenLog","IMsmMerge::OpenLog","OpenLog","OpenLog method","OpenLog method","IMsmMerge interface","_msi_openlog_function","mergemod/IMsmMerge::OpenLog","setup.imsmmerge_openlog"]
old-location: setup\imsmmerge_openlog.htm
tech.root: setup
ms.assetid: b34e7f28-2cf3-4cc7-9a39-e1da6fb8c788
ms.date: 12/05/2018
ms.keywords: IMsmMerge interface,OpenLog method, IMsmMerge.OpenLog, IMsmMerge::OpenLog, OpenLog, OpenLog method, OpenLog method,IMsmMerge interface, _msi_openlog_function, mergemod/IMsmMerge::OpenLog, setup.imsmmerge_openlog
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
 - IMsmMerge::OpenLog
 - mergemod/IMsmMerge::OpenLog
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
 - IMsmMerge.OpenLog
---

# IMsmMerge::OpenLog


## -description

The 
<b>OpenLog</b> method opens a log file that receives progress and error messages. If the log file already exists, the installer appends new messages. If the log file does not exist, the installer creates a log file. For more information, see the 
<a href="/windows/desktop/Msi/merge-openlog">OpenLog</a> method of the 
<a href="/windows/desktop/Msi/merge-object">Merge</a> object. 

<b>IMsmMerge2::OpenLog</b>    Mergemod.dll version 2.0 or later.<div> </div><b>IMsmMerge::OpenLog</b>      All Mergemod.dll versions.

## -parameters

### -param Path [in]

Fully qualified file name pointing to a file to open or create. A <b>LPCWSTR</b> may be used in place of a <b>BSTR</b>.

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
<dt><b>ERROR_TOO_MANY_OPEN_FILES as HRESULT </b></dt>
</dl>
</td>
<td width="60%">
There is already a log file open.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_OPEN_FAILED as HRESULT </b></dt>
</dl>
</td>
<td width="60%">
The file could not be opened or created.

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

## -remarks

This function opens a log file to receive progress and error messages. If the log file already exists, new messages get appended to the log. If the log file does not exist it is created.

Clients may send their own messages to this log file using <a href="/windows/desktop/api/mergemod/nf-mergemod-imsmmerge-log">Log</a>.

## -see-also

<a href="/windows/desktop/Msi/merge-module-automation">Merge Module Automation</a>