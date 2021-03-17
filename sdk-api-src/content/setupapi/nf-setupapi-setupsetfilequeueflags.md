---
UID: NF:setupapi.SetupSetFileQueueFlags
title: SetupSetFileQueueFlags function (setupapi.h)
description: The SetupSetFileQueueFlags function sets the flags on a setup file queue.
helpviewer_keywords: ["SPQ_FLAG_ABORT_IF_UNSIGNED","SPQ_FLAG_BACKUP_AWARE","SPQ_FLAG_VALID","SetupSetFileQueueFlags","SetupSetFileQueueFlags function [Setup API]","_setupapi_setupsetfilequeueflags","setup.setupsetfilequeueflags","setupapi/SetupSetFileQueueFlags"]
old-location: setup\setupsetfilequeueflags.htm
tech.root: setup
ms.assetid: 63a4dfbb-bd48-4183-9e7d-ce337f2707fb
ms.date: 12/05/2018
ms.keywords: SPQ_FLAG_ABORT_IF_UNSIGNED, SPQ_FLAG_BACKUP_AWARE, SPQ_FLAG_VALID, SetupSetFileQueueFlags, SetupSetFileQueueFlags function [Setup API], _setupapi_setupsetfilequeueflags, setup.setupsetfilequeueflags, setupapi/SetupSetFileQueueFlags
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
 - SetupSetFileQueueFlags
 - setupapi/SetupSetFileQueueFlags
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
 - SetupSetFileQueueFlags
---

# SetupSetFileQueueFlags function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupSetFileQueueFlags</b> function sets the flags on a setup file queue.

## -parameters

### -param FileQueue [in]

Handle to an open setup file queue.

### -param FlagMask [in]

Mask of valid flags. 



<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SPQ_FLAG_VALID"></a><a id="spq_flag_valid"></a><dl>
<dt><b>SPQ_FLAG_VALID</b></dt>
<dt>0x001</dt>
</dl>
</td>
<td width="60%">
Mask for use with SPQ_FLAG_BACKUP_AWARE.

</td>
</tr>
</table>

### -param Flags [in]

Flags for use with 
<b>SetupSetFileQueueFlags</b> and returned by 
<a href="/windows/desktop/api/setupapi/nf-setupapi-setupgetfilequeueflags">SetupGetFileQueueFlags</a>. 



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

If the function fails, the return value is (0) zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>