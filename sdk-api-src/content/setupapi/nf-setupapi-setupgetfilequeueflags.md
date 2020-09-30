---
UID: NF:setupapi.SetupGetFileQueueFlags
title: SetupGetFileQueueFlags function (setupapi.h)
description: The SetupGetFileQueueFlags function gets the flags from a setup file queue.
helpviewer_keywords: ["SPQ_FLAG_ABORT_IF_UNSIGNED","SPQ_FLAG_BACKUP_AWARE","SetupGetFileQueueFlags","SetupGetFileQueueFlags function [Setup API]","_setupapi_setupgetfilequeueflags","setup.setupgetfilequeueflags","setupapi/SetupGetFileQueueFlags"]
old-location: setup\setupgetfilequeueflags.htm
tech.root: setup
ms.assetid: cb5a7cd8-870c-4880-bb29-6e24a098c35e
ms.date: 12/05/2018
ms.keywords: SPQ_FLAG_ABORT_IF_UNSIGNED, SPQ_FLAG_BACKUP_AWARE, SetupGetFileQueueFlags, SetupGetFileQueueFlags function [Setup API], _setupapi_setupgetfilequeueflags, setup.setupgetfilequeueflags, setupapi/SetupGetFileQueueFlags
req.header: setupapi.h
req.include-header: 
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
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetupGetFileQueueFlags
 - setupapi/SetupGetFileQueueFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
api_name:
 - SetupGetFileQueueFlags
---

# SetupGetFileQueueFlags function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupGetFileQueueFlags</b> function gets the flags from a setup file queue.

## -parameters

### -param FileQueue [in]

Handle to an open setup file queue.

### -param Flags [out]

Pointer to location that contains the flag set with 
<a href="/windows/desktop/api/setupapi/nf-setupapi-setupsetfilequeueflags">SetupSetFileQueueFlags</a> and returned by 
<b>SetupGetFileQueueFlags</b>. 



<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SPQ_FLAG_BACKUP_AWARE"></a><a id="spq_flag_backup_aware"></a><dl>
<dt><b>SPQ_FLAG_BACKUP_AWARE</b></dt>
<dt>0x001</dt>
</dl>
</td>
<td width="60%">
If this flag is set, 
<a href="/windows/desktop/api/setupapi/nf-setupapi-setupcommitfilequeuea">SetupCommitFileQueue</a> issues backup notifications.

</td>
</tr>
<tr>
<td width="40%"><a id="SPQ_FLAG_ABORT_IF_UNSIGNED"></a><a id="spq_flag_abort_if_unsigned"></a><dl>
<dt><b>SPQ_FLAG_ABORT_IF_UNSIGNED</b></dt>
<dt>0X002</dt>
</dl>
</td>
<td width="60%">
For internal use only.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is 0 (zero). To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>