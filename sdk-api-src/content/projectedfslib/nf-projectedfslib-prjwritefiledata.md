---
UID: NF:projectedfslib.PrjWriteFileData
title: PrjWriteFileData function (projectedfslib.h)
description: The PrjWriteFileData function provides the data requested in an invocation of the PRJ_GET_FILE_DATA_CB callback. (PrjWriteFileData)
helpviewer_keywords: ["PrjWriteFileData","PrjWriteFileData function","ProjFS.prjwritefiledata","projectedfslib/PrjWriteFileData"]
old-location: projfs\prjwritefiledata.htm
tech.root: ProjFS
ms.assetid: A09D8E74-D574-41C6-A586-86E03839DA89
ms.date: 08/03/2022
ms.keywords: PrjWriteFileData, PrjWriteFileData function, ProjFS.prjwritefiledata, projectedfslib/PrjWriteFileData
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
req.lib: ProjectedFSLib.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: RS5, 19H1
f1_keywords:
 - PrjWriteFileData
 - projectedfslib/PrjWriteFileData
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
 - PrjWriteFileData
---

# PrjWriteFileData function


## -description

Provides the data requested in an invocation of the <a href="/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb">PRJ_GET_FILE_DATA_CB</a> callback.

## -parameters

### -param namespaceVirtualizationContext [in]

Opaque handle for the virtualization instance. 


If the provider is servicing a <a href="/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb">PRJ_GET_FILE_DATA_CB</a> callback, this must be the value from the VirtualizationInstanceHandle member of the callbackData passed to the provider in the callback.

### -param dataStreamId [in]

Identifier for the data stream to write to. 


If the provider is servicing a <a href="/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb">PRJ_GET_FILE_DATA_CB</a> callback, this must be the value from the DataStreamId member of the callbackData passed to the provider in the callback.

### -param buffer [in]

Pointer to a buffer containing the data to write. The buffer must be at least as large as the value of the length parameter in bytes. The provider should use <a href="/windows/desktop/api/projectedfslib/nf-projectedfslib-prjallocatealignedbuffer">PrjAllocateAlignedBuffer</a> to ensure that the buffer meets the storage device's alignment requirements.

### -param byteOffset [in]

Byte offset from the beginning of the file at which to write the data.

### -param length [in]

The number of bytes to write to the file.

## -returns

HRESULT_FROM_WIN32(ERROR_OFFSET_ALIGNMENT_VIOLATION) indicates that the user's handle was opened for unbuffered I/O and byteOffset is not aligned to the sector size of the storage device.

## -remarks

The provider uses this routine to provide the data requested in an invocation of its <a href="/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb">PRJ_GET_FILE_DATA_CB</a> callback. 


The provider’s <a href="/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb">PRJ_GET_FILE_DATA_CB</a> callback is invoked when the system needs to ensure that a file contains data. When the provider calls <a href="/windows/desktop/api/projectedfslib/nf-projectedfslib-prjwritefiledata">PrjWriteFileData</a> to supply the requested data the system uses the user’s FILE_OBJECT to write that data to the file. However the system cannot control whether that FILE_OBJECT was opened for buffered or unbuffered I/O. If the FILE_OBJECT was opened for unbuffered I/O, reads and writes to the file must adhere to certain alignment requirements. The provider can meet those alignment requirements by doing two things: 
<ul>
<li>Use <a href="/windows/desktop/api/projectedfslib/nf-projectedfslib-prjallocatealignedbuffer">PrjAllocateAlignedBuffer</a> to allocate the buffer to pass to buffer.</li>
<li>Ensure that byteOffset and length are integer multiples of the storage device’s alignment requirement (length does not have to meet this requirement if byteOffset + length is equal to the end of the file). The provider can use <a href="/windows/desktop/api/projectedfslib/nf-projectedfslib-prjgetvirtualizationinstanceinfo">PrjGetVirtualizationInstanceInfo</a> to retrieve the storage device’s alignment requirement.</li>
</ul>


The system leaves it up to the provider to calculate proper alignment because when processing a <a href="/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb">PRJ_GET_FILE_DATA_CB</a> callback the provider may opt to return the requested data across multiple <a href="/windows/desktop/api/projectedfslib/nf-projectedfslib-prjwritefiledata">PrjWriteFileData</a> calls, each returning part of the total requested data. 

Note that if the provider is going to write the entire file in a single call to <a href="/windows/desktop/api/projectedfslib/nf-projectedfslib-prjwritefiledata">PrjWriteFileData</a>, i.e. from byteOffset = 0 to length = size of the file, the provider does not have to do any alignment calculations. However it must still use <a href="/windows/desktop/api/projectedfslib/nf-projectedfslib-prjallocatealignedbuffer">PrjAllocateAlignedBuffer</a> to ensure that buffer meets the storage device's alignment requirements. See the <a href="/windows/desktop/FileIO/file-buffering">File Buffering</a> topic for more information on buffered vs unbuffered I/O.
