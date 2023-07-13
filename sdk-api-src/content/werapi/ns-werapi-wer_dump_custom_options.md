---
UID: NS:werapi._WER_DUMP_CUSTOM_OPTIONS
tech.root: wer
title: WER_DUMP_CUSTOM_OPTIONS (werapi.h)
ms.date: 12/05/2018
targetos: Windows
description: Specifies custom minidump information to be collected by the WerReportAddDump function.
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

Specifies custom minidump information to be collected by the <a href="/windows/desktop/api/werapi/nf-werapi-werreportadddump">WerReportAddDump</a> function.

## -struct-fields

### -field dwSize

The size of the structure, in bytes.

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

The type information to include in the minidump. You can specify one or more of the <a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type">MINIDUMP_TYPE</a> flags. 

This member is valid only if <b>dwMask</b> contains WER_DUMP_MASK_DUMPTYPE.

### -field bOnlyThisThread

If this member is <b>TRUE</b> and <b>dwMask</b> contains WER_DUMP_MASK_ONLY_THISTHREAD, the minidump is to be collected only for the calling thread.

### -field dwExceptionThreadFlags

The type of thread information to include in the minidump. You can specify one or more of the <a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-thread_write_flags">THREAD_WRITE_FLAGS</a> flags.

This member is valid only if <b>dwMask</b> contains WER_DUMP_MASK_THREADFLAGS.

### -field dwOtherThreadFlags

The type of thread information to include in the minidump. You can specify one or more of the <a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-thread_write_flags">THREAD_WRITE_FLAGS</a> flags.

This member is valid only if <b>dwMask</b> contains WER_DUMP_MASK_OTHERTHREADFLAGS.

### -field dwExceptionThreadExFlags

The type of thread information to include in the minidump. You can specify one or more of the <a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-thread_write_flags">THREAD_WRITE_FLAGS</a> flags.

This member is valid only if <b>dwMask</b> contains WER_DUMP_MASK_THREADFLAGS_EX.

### -field dwOtherThreadExFlags

The type of thread information to include in the minidump. You can specify one or more of the <a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-thread_write_flags">THREAD_WRITE_FLAGS</a> flags.

This member is valid only if <b>dwMask</b> contains WER_DUMP_MASK_OTHERTHREADFLAGS_EX.

### -field dwPreferredModuleFlags

The type of module information to include in the minidump for modules specified in the <b>wzPreferredModuleList</b> member. You can specify one or more of the <a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-module_write_flags">MODULE_WRITE_FLAGS</a> flags.

This member is valid only if <b>dwMask</b> contains WER_DUMP_MASK_PREFERRED_MODULESFLAGS.

### -field dwOtherModuleFlags

The type of module information to include in the minidump. You can specify one or more of the <a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-module_write_flags">MODULE_WRITE_FLAGS</a> flags.

This member is valid only if <b>dwMask</b> contains WER_DUMP_MASK_OTHER_MODULESFLAGS.

### -field wzPreferredModuleList

A list of module names (do not include the path) to which the <b>dwPreferredModuleFlags</b> flags apply. Each name must be null-terminated, and the list must be terminated with two null characters (for example, module1.dll\0module2.dll\0\0).

To specify that all modules are preferred, set this member to "*\0\0". If you include * in a list with other module names, the * is ignored. 

This member is valid only if <b>dwMask</b> contains WER_DUMP_MASK_PREFERRED_MODULE_LIST.

## -remarks

The flags specified in this structure have a direct correlation to flags passed in the   <a href="/windows/desktop/api/minidumpapiset/nc-minidumpapiset-minidump_callback_routine">MiniDumpCallback</a> callback function (see <a href="/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump">MiniDumpWriteDump</a>) when WER generates the dump file.

If the minidump's callback input type is <b>ThreadCallback</b> (see the <b>CallbackType</b> member of <a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_callback_output">MINIDUMP_CALLBACK_INPUT</a>), the <b>ThreadWriteFlags</b> member of <a href="/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_callback_output">MINIDUMP_CALLBACK_OUTPUT</a> is set to the flags specified in the <b>dwExceptionThreadFlags</b>, <b>dwExceptionThreadExFlags</b>, <b>dwOtherThreadFlags</b>, or <b>dwOtherThreadExFlags</b> members. If the callback is for the crashing thread, the <b>dwExceptionThreadFlags</b> or <b>dwExceptionThreadExFlags</b> flags are used; otherwise, the  <b>dwOtherThreadFlags</b> or <b>dwOtherThreadExFlags</b> flags are used.

If the callback input type is <b>ModuleCallback</b>, the  <b>ModuleWriteFlags</b> member of <a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_callback_output">MINIDUMP_CALLBACK_OUTPUT</a> is set to the flags specified in the <b>dwPreferredModuleFlags</b> or <b>dwOtherModuleFlags</b> members. If the callback is for a module on the preferred modules list, the <b>dwPreferredModuleFlags</b> flags are used; otherwise, the <b>dwOtherModuleFlags</b> flags are used.

## -see-also

<a href="/windows/desktop/api/werapi/nf-werapi-werreportadddump">WerReportAddDump</a>