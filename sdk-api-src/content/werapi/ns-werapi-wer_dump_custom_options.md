---
UID: NS:werapi._WER_DUMP_CUSTOM_OPTIONS
tech.root: wer
title: WER_DUMP_CUSTOM_OPTIONS (werapi.h)
ms.date: 07/26/2023
targetos: Windows
description: Specifies custom Windows Error Reporting (WER) minidump information to be collected by the WerReportAddDump function.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
ms.keywords: '*PWER_DUMP_CUSTOM_OPTIONS, PWER_DUMP_CUSTOM_OPTIONS, PWER_DUMP_CUSTOM_OPTIONS structure pointer [Windows Error Reporting], WER_DUMP_CUSTOM_OPTIONS, WER_DUMP_CUSTOM_OPTIONS structure [Windows Error Reporting], WER_DUMP_MASK_DUMPTYPE, WER_DUMP_MASK_ONLY_THISTHREAD, WER_DUMP_MASK_OTHERTHREADFLAGS, WER_DUMP_MASK_OTHERTHREADFLAGS_EX, WER_DUMP_MASK_OTHER_MODULESFLAGS, WER_DUMP_MASK_PREFERRED_MODULESFLAGS, WER_DUMP_MASK_PREFERRED_MODULE_LIST, WER_DUMP_MASK_THREADFLAGS, WER_DUMP_MASK_THREADFLAGS_EX, base.wer_dump_custom_options, wer.wer_dump_custom_options, werapi/PWER_DUMP_CUSTOM_OPTIONS, werapi/WER_DUMP_CUSTOM_OPTIONS'
req.header: werapi.h
old-location: wer\wer_dump_custom_options.htm
ms.assetid: 6ea32573-ac1a-4f9b-b4ba-b5767927924f
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.irql: 
req.typenames: WER_DUMP_CUSTOM_OPTIONS, *PWER_DUMP_CUSTOM_OPTIONS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WER_DUMP_CUSTOM_OPTIONS
 - werapi/_WER_DUMP_CUSTOM_OPTIONS
 - PWER_DUMP_CUSTOM_OPTIONS
 - werapi/PWER_DUMP_CUSTOM_OPTIONS
 - WER_DUMP_CUSTOM_OPTIONS
 - werapi/WER_DUMP_CUSTOM_OPTIONS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Werapi.h
api_name:
 - WER_DUMP_CUSTOM_OPTIONS
helpviewer_keywords: ["*PWER_DUMP_CUSTOM_OPTIONS","PWER_DUMP_CUSTOM_OPTIONS","PWER_DUMP_CUSTOM_OPTIONS structure pointer [Windows Error Reporting]","WER_DUMP_CUSTOM_OPTIONS","WER_DUMP_CUSTOM_OPTIONS structure [Windows Error Reporting]","WER_DUMP_MASK_DUMPTYPE","WER_DUMP_MASK_ONLY_THISTHREAD","WER_DUMP_MASK_OTHERTHREADFLAGS","WER_DUMP_MASK_OTHERTHREADFLAGS_EX","WER_DUMP_MASK_OTHER_MODULESFLAGS","WER_DUMP_MASK_PREFERRED_MODULESFLAGS","WER_DUMP_MASK_PREFERRED_MODULE_LIST","WER_DUMP_MASK_THREADFLAGS","WER_DUMP_MASK_THREADFLAGS_EX","base.wer_dump_custom_options","wer.wer_dump_custom_options","werapi/PWER_DUMP_CUSTOM_OPTIONS","werapi/WER_DUMP_CUSTOM_OPTIONS"]
---

# WER_DUMP_CUSTOM_OPTIONS structure

## -description

Specifies custom [Windows Error Reporting](../_wer/index.md) (WER) minidump information to be collected by the [WerReportAddDump](nf-werapi-werreportadddump.md) function.

## -struct-fields

### -field dwSize

The size of the structure, in bytes.

### -field dwMask

A mask that controls which options are valid in this structure. You can specify one or more of the following values:

- WER_DUMP_MASK_DUMPTYPE
- WER_DUMP_MASK_ONLY_THISTHREAD
- WER_DUMP_MASK_OTHER_MODULESFLAGS
- WER_DUMP_MASK_OTHERTHREADFLAGS
- WER_DUMP_MASK_OTHERTHREADFLAGS_EX
- WER_DUMP_MASK_PREFERRED_MODULE_LIST
- WER_DUMP_MASK_PREFERRED_MODULESFLAGS
- WER_DUMP_MASK_THREADFLAGS
- WER_DUMP_MASK_THREADFLAGS_EX

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

### -field wzPreferredModuleList

A list of module names (do not include the path) to which the **dwPreferredModuleFlags** flags apply. Each name must be null-terminated, and the list must be terminated with two null characters (for example, module1.dll\0module2.dll\0\0).

To specify that all modules are preferred, set this member to `*\0\0`. If you include `*` in a list with other module names, the `*` is ignored.

This member is valid only if **dwMask** contains WER_DUMP_MASK_PREFERRED_MODULE_LIST.

## -remarks

The flags specified in this structure have a direct correlation to flags passed in the [MINIDUMP_CALLBACK_ROUTINE callback function](../minidumpapiset/nc-minidumpapiset-minidump_callback_routine.md) callback function (see [MiniDumpWriteDump function](../minidumpapiset/nf-minidumpapiset-minidumpwritedump.md)) when WER generates the dump file.

If the minidump's callback input type is **ThreadCallback** (see the **CallbackType** member of [MINIDUMP_CALLBACK_INPUT structure](../minidumpapiset/ns-minidumpapiset-minidump_callback_input.md)), the **ThreadWriteFlags** member of [MINIDUMP_CALLBACK_OUTPUT structure](../minidumpapiset/ns-minidumpapiset-minidump_callback_output.md) is set to the flags specified in the **dwExceptionThreadFlags**, **dwExceptionThreadExFlags**, **dwOtherThreadFlags**, or **dwOtherThreadExFlags** members. If the callback is for the crashing thread, the **dwExceptionThreadFlags** or **dwExceptionThreadExFlags** flags are used; otherwise, the  **dwOtherThreadFlags** or **dwOtherThreadExFlags** flags are used.

If the callback input type is **ModuleCallback**, the  **ModuleWriteFlags** member of [MINIDUMP_CALLBACK_OUTPUT structure](../minidumpapiset/ns-minidumpapiset-minidump_callback_output.md) is set to the flags specified in the **dwPreferredModuleFlags** or **dwOtherModuleFlags** members. If the callback is for a module on the preferred modules list, the **dwPreferredModuleFlags** flags are used; otherwise, the **dwOtherModuleFlags** flags are used.

## -see-also

[WerReportAddDump function](nf-werapi-werreportadddump.md), [Windows Error Reporting](/windows/desktop/wer)