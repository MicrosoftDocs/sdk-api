---
UID: NS:projectedfslib.PRJ_CALLBACK_DATA
title: PRJ_CALLBACK_DATA (projectedfslib.h)
description: Defines the standard information passed to a provider for every operation callback.
helpviewer_keywords: ["PRJ_CALLBACK_DATA","PRJ_CALLBACK_DATA structure","ProjFS.prj_callback_data","projectedfslib/PRJ_CALLBACK_DATA"]
old-location: projfs\prj_callback_data.htm
tech.root: ProjFS
ms.assetid: 569204FF-97F5-4FE2-9885-94C88AB5A6FE
ms.date: 12/05/2018
ms.keywords: PRJ_CALLBACK_DATA, PRJ_CALLBACK_DATA structure, ProjFS.prj_callback_data, projectedfslib/PRJ_CALLBACK_DATA
req.header: projectedfslib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server [desktop apps only]
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
targetos: Windows
req.typenames: PRJ_CALLBACK_DATA
req.redist: 
ms.custom: RS5, 19H1
f1_keywords:
 - PRJ_CALLBACK_DATA
 - projectedfslib/PRJ_CALLBACK_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - projectedfslib.h
api_name:
 - PRJ_CALLBACK_DATA
---

# PRJ_CALLBACK_DATA structure


## -description

Defines the standard information passed to a provider for every operation callback.

## -struct-fields

### -field Size

Size in bytes of this structure. The provider must not attempt to access any field of this structure that is located beyond this value.

### -field Flags

Callback-specific flags.

### -field NamespaceVirtualizationContext

Opaque handle to the virtualization instance that is sending the callback.

### -field CommandId

A value that uniquely identifies a particular invocation of a callback. The provider uses this value: 


<ul>
<li>In calls to <a href="/windows/desktop/api/projectedfslib/nf-projectedfslib-prjcompletecommand">PrjCompleteCommand</a> to signal completion of a callback from which it earlier returned HRESULT_FROM_WIN32(ERROR_IO_PENDING).</li>
<li>When ProjFS sends a <a href="/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_cancel_command_cb">PRJ_CANCEL_COMMAND_CB</a> callback. The commandId in the <i>PRJ_CANCEL_COMMAND_CB</i> call identifies an earlier invocation of a callback that the provider should cancel.</li>
</ul>

### -field FileId

A value that uniquely identifies the file handle for the callback.

### -field DataStreamId

A value that uniquely identifies an open data stream for the callback.

### -field FilePathName

The path to the target file. This is a null-terminated string of Unicode characters. This path is always specified relative to the virtualization root.

### -field VersionInfo

Version information if the target of the callback is a placeholder or partial file.

### -field TriggeringProcessId

The process identifier for the process that triggered this callback. If this information is not available, this will be 0. Callbacks that supply this information include: <a href="/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_placeholder_info_cb">PRJ_GET_PLACEHOLDER_INFO_CB</a>, 
<a href="/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb">PRJ_GET_FILE_DATA_CB</a>, and 
<a href="/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_notification_cb">PRJ_NOTIFICATION_CB</a>.

### -field TriggeringProcessImageFileName

A null-terminated Unicode string specifying the image file name corresponding to TriggeringProcessId. If TriggeringProcessId is 0 this will be NULL.

### -field InstanceContext

A pointer to context information defined by the provider. The provider passes this context in the instanceContext parameter of <a href="/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstartvirtualizing">PrjStartVirtualizing</a>. 


If the provider did not specify such a context, this value will be NULL.

