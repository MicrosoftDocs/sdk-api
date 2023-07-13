---
UID: NS:werapi._WER_DUMP_CUSTOM_OPTIONS_V2
tech.root: wer
title: WER_DUMP_CUSTOM_OPTIONS_V2 (werapi.h)
ms.date: 07/12/2023
targetos: Windows
description: Specifies custom minidump information to be collected in the background (without pausing the process) by the [**PssCaptureSnapshot**](../processsnapshot/nf-processsnapshot-psscapturesnapshot.md) function.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
ms.keywords: '*PWER_DUMP_CUSTOM_OPTIONS_V2, PWER_DUMP_CUSTOM_OPTIONS_V2, PWER_DUMP_CUSTOM_OPTIONS_V2 structure pointer [Windows Error Reporting], WER_DUMP_CUSTOM_OPTIONS_V2, WER_DUMP_CUSTOM_OPTIONS_V2 structure [Windows Error Reporting], WER_DUMP_MASK_DUMPTYPE, WER_DUMP_MASK_ONLY_THISTHREAD, WER_DUMP_MASK_OTHERTHREADFLAGS, WER_DUMP_MASK_OTHERTHREADFLAGS_EX, WER_DUMP_MASK_OTHER_MODULESFLAGS, WER_DUMP_MASK_PREFERRED_MODULESFLAGS, WER_DUMP_MASK_PREFERRED_MODULE_LIST, WER_DUMP_MASK_THREADFLAGS, WER_DUMP_MASK_THREADFLAGS_EX, base.wer_dump_custom_options_v2, wer.wer_dump_custom_options_v2, werapi/PWER_DUMP_CUSTOM_OPTIONS_V2, werapi/WER_DUMP_CUSTOM_OPTIONS_V2'
req.header: werapi.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.target-type: Windows
req.typenames: WER_DUMP_CUSTOM_OPTIONS_V2, *PWER_DUMP_CUSTOM_OPTIONS_V2
typedef_isUnnamed: false
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - werapi.h
api_name:
 - _WER_DUMP_CUSTOM_OPTIONS_V2
 - PWER_DUMP_CUSTOM_OPTIONS_V2
 - WER_DUMP_CUSTOM_OPTIONS_V2
f1_keywords:
 - _WER_DUMP_CUSTOM_OPTIONS_V2
 - werapi/_WER_DUMP_CUSTOM_OPTIONS_V2
 - PWER_DUMP_CUSTOM_OPTIONS_V2
 - werapi/PWER_DUMP_CUSTOM_OPTIONS_V2
 - WER_DUMP_CUSTOM_OPTIONS_V2
 - werapi/WER_DUMP_CUSTOM_OPTIONS_V2
dev_langs:
 - c++
helpviewer_keywords: ["*PWER_DUMP_CUSTOM_OPTIONS_V2","PWER_DUMP_CUSTOM_OPTIONS_V2","PWER_DUMP_CUSTOM_OPTIONS_V2 structure pointer [Windows Error Reporting]","WER_DUMP_CUSTOM_OPTIONS_V2","WER_DUMP_CUSTOM_OPTIONS_V2 structure [Windows Error Reporting]","WER_DUMP_MASK_DUMPTYPE","WER_DUMP_MASK_ONLY_THISTHREAD","WER_DUMP_MASK_OTHERTHREADFLAGS","WER_DUMP_MASK_OTHERTHREADFLAGS_EX","WER_DUMP_MASK_OTHER_MODULESFLAGS","WER_DUMP_MASK_PREFERRED_MODULESFLAGS","WER_DUMP_MASK_PREFERRED_MODULE_LIST","WER_DUMP_MASK_THREADFLAGS","WER_DUMP_MASK_THREADFLAGS_EX","base.wer_dump_custom_options_v2","wer.wer_dump_custom_options_v2","werapi/PWER_DUMP_CUSTOM_OPTIONS_V2","werapi/WER_DUMP_CUSTOM_OPTIONS_V2"]
---

# WER_DUMP_CUSTOM_OPTIONS_V2 structure

## -description

Specifies custom minidump information to be collected by the <a href="/windows/desktop/api/werapi/nf-werapi-werreportadddump">WerReportAddDump</a> function.

## -struct-fields

### -field dwSize

The size of the structure, in bytes.

### -field dwMask

A mask that controls which options are valid in this structure. You can specify one or more of the following values:
#### WER_DUMP_MASK_DUMPTYPE

<a id="WER_DUMP_MASK_ONLY_THISTHREAD"></a>
<a id="wer_dump_mask_only_thisthread"></a>

### -field dwMask

A mask that controls which options are valid in this structure. You can specify one or more of the following values:

<a id="WER_DUMP_MASK_DUMPTYPE"></a>
<a id="wer_dump_mask_dumptype"></a>

#### WER_DUMP_MASK_DUMPTYPE

<a id="WER_DUMP_MASK_ONLY_THISTHREAD"></a>
<a id="wer_dump_mask_only_thisthread"></a>

#### WER_DUMP_MASK_ONLY_THISTHREAD

<a id="WER_DUMP_MASK_OTHER_MODULESFLAGS"></a>
<a id="wer_dump_mask_other_modulesflags"></a>

#### WER_DUMP_MASK_OTHER_MODULESFLAGS

<a id="WER_DUMP_MASK_OTHERTHREADFLAGS"></a>
<a id="wer_dump_mask_otherthreadflags"></a>

#### WER_DUMP_MASK_OTHERTHREADFLAGS

<a id="WER_DUMP_MASK_OTHERTHREADFLAGS_EX"></a>
<a id="wer_dump_mask_otherthreadflags_ex"></a>

#### WER_DUMP_MASK_OTHERTHREADFLAGS_EX

<a id="WER_DUMP_MASK_PREFERRED_MODULE_LIST"></a>
<a id="wer_dump_mask_preferred_module_list"></a>

#### WER_DUMP_MASK_PREFERRED_MODULE_LIST

<a id="WER_DUMP_MASK_PREFERRED_MODULESFLAGS"></a>
<a id="wer_dump_mask_preferred_modulesflags"></a>

#### WER_DUMP_MASK_PREFERRED_MODULESFLAGS

<a id="WER_DUMP_MASK_THREADFLAGS"></a>
<a id="wer_dump_mask_threadflags"></a>

#### WER_DUMP_MASK_THREADFLAGS

<a id="WER_DUMP_MASK_THREADFLAGS_EX"></a>
<a id="wer_dump_mask_threadflags_ex"></a>

#### WER_DUMP_MASK_THREADFLAGS_EX

### -field dwDumpFlags

The type information to include in the minidump. You can specify one or more of the [MINIDUMP_TYPE](../minidumpapiset/ne-minidumpapiset-minidump_type.md) flags.

This member is valid only if **dwMask** contains WER_DUMP_MASK_DUMPTYPE.

### -field bOnlyThisThread

If this member is **TRUE** and **dwMask** contains WER_DUMP_MASK_ONLY_THISTHREAD, the minidump is to be collected only for the calling thread.

### -field dwExceptionThreadFlags

The type of thread information to include in the minidump. You can specify one or more of the [THREAD_WRITE_FLAGS](../minidumpapiset/ne-minidumpapiset-thread_write_flags.md) flags.

This member is valid only if **dwMask** contains WER_DUMP_MASK_THREADFLAGS.

### -field dwOtherThreadFlags

The type of thread information to include in the minidump. You can specify one or more of the [THREAD_WRITE_FLAGS](../minidumpapiset/ne-minidumpapiset-thread_write_flags.md) flags.

This member is valid only if **dwMask** contains WER_DUMP_MASK_OTHERTHREADFLAGS.

### -field dwExceptionThreadExFlags

The type of thread information to include in the minidump. You can specify one or more of the [THREAD_WRITE_FLAGS](../minidumpapiset/ne-minidumpapiset-thread_write_flags.md) flags.

This member is valid only if **dwMask** contains WER_DUMP_MASK_THREADFLAGS_EX.

### -field dwOtherThreadExFlags

The type of thread information to include in the minidump. You can specify one or more of the [THREAD_WRITE_FLAGS](../minidumpapiset/ne-minidumpapiset-thread_write_flags.md) flags.

This member is valid only if **dwMask** contains WER_DUMP_MASK_OTHERTHREADFLAGS_EX.

### -field dwPreferredModuleFlags

The type of module information to include in the minidump for modules specified in the **wzPreferredModuleList** member. You can specify one or more of the [MODULE_WRITE_FLAGS](../minidumpapiset/ne-minidumpapiset-module_write_flags.md) flags.

This member is valid only if **dwMask** contains WER_DUMP_MASK_PREFERRED_MODULESFLAGS.

### -field dwOtherModuleFlags

The type of module information to include in the minidump. You can specify one or more of the [MODULE_WRITE_FLAGS](../minidumpapiset/ne-minidumpapiset-module_write_flags.md) flags.

This member is valid only if **dwMask** contains WER_DUMP_MASK_OTHER_MODULESFLAGS.

### -field wzPreferredModuleList[WER_MAX_PREFERRED_MODULES_BUFFER]

A list of module names (do not include the path) to which the **dwPreferredModuleFlags** flags apply. Each name must be null-terminated, and the list must be terminated with two null characters (for example, module1.dll\0module2.dll\0\0).

To specify that all modules are preferred, set this member to `*\0\0`. If you include `*` in a list with other module names, the `*` is ignored.

This member is valid only if **dwMask** contains WER_DUMP_MASK_PREFERRED_MODULE_LIST.

### -field dwPreferredModuleResetFlags

The preferred type of module information to include in the minidump for modules specified in the **wzPreferredModuleList** member. You can specify one or more of the [MODULE_WRITE_FLAGS](../minidumpapiset/ne-minidumpapiset-module_write_flags.md) flags.

This member is valid only if **dwMask** contains WER_DUMP_MASK_PREFERRED_MODULESFLAGS.

### -field dwOtherModuleResetFlags

Other types of module information to include in the minidump for modules specified in the **wzPreferredModuleList** member. You can specify one or more of the [MODULE_WRITE_FLAGS](../minidumpapiset/ne-minidumpapiset-module_write_flags.md) flags.

This member is valid only if **dwMask** contains WER_DUMP_MASK_PREFERRED_MODULESFLAGS.

## -remarks

## -see-also

[WerReportAddDump function](nf-werapi-werreportadddump.md)