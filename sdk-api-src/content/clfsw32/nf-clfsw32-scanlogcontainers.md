---
UID: NF:clfsw32.ScanLogContainers
title: ScanLogContainers function (clfsw32.h)
description: Enumerates log containers. Call this function repeatedly to iterate over all log containers.
helpviewer_keywords: ["CLFS_SCAN_BACKWARD","CLFS_SCAN_CLOSE","CLFS_SCAN_FORWARD","CLFS_SCAN_INIT","ScanLogContainers","ScanLogContainers function [Files]","clfsw32/ScanLogContainers","fs.scanlogcontainers"]
old-location: fs\scanlogcontainers.htm
tech.root: fs
ms.assetid: a3a374ab-e5e9-47c0-9a62-d880823035b5
ms.date: 12/05/2018
ms.keywords: CLFS_SCAN_BACKWARD, CLFS_SCAN_CLOSE, CLFS_SCAN_FORWARD, CLFS_SCAN_INIT, ScanLogContainers, ScanLogContainers function [Files], clfsw32/ScanLogContainers, fs.scanlogcontainers
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
req.lib: Clfsw32.lib
req.dll: Clfsw32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ScanLogContainers
 - clfsw32/ScanLogContainers
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Clfsw32.dll
api_name:
 - ScanLogContainers
---

# ScanLogContainers function


## -description

Enumerates log containers. Call this function repeatedly to iterate over all log containers.

## -parameters

### -param pcxScan [in, out]

A pointer to a client-allocated <a href="/windows/win32/api/clfs/ns-clfs-cls_scan_context~r1">CLFS_SCAN_CONTEXT</a> structure  that  the <a href="/windows/desktop/api/clfsw32/nf-clfsw32-createlogcontainerscancontext">CreateLogContainerScanContext</a> function initializes.

### -param eScanMode [in]

The mode  for  containers  to  be scanned.  

Containers can be scanned in any  of the following <a href="/previous-versions/windows/desktop/clfs/clfs-scan-mode-constants">CLFS_SCAN_MODE</a> modes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CLFS_SCAN_INIT"></a><a id="clfs_scan_init"></a><dl>
<dt><b>CLFS_SCAN_INIT</b></dt>
</dl>
</td>
<td width="60%">
Reinitializes the scan context, but does not allocate associated storage.  

The initialization is destructive, because all  data that is stored in the current scan context is lost.

</td>
</tr>
<tr>
<td width="40%"><a id="CLFS_SCAN_CLOSE"></a><a id="clfs_scan_close"></a><dl>
<dt><b>CLFS_SCAN_CLOSE</b></dt>
</dl>
</td>
<td width="60%">
Uninitializes the scan context, and deallocates  system storage that is associated with a scan context.

</td>
</tr>
<tr>
<td width="40%"><a id="CLFS_SCAN_FORWARD"></a><a id="clfs_scan_forward"></a><dl>
<dt><b>CLFS_SCAN_FORWARD</b></dt>
</dl>
</td>
<td width="60%">
Causes the next call to <b>ScanLogContainers</b> to proceed  in a forward direction. 

Cannot be used if <b>CLFS_SCAN_BACKWARD</b> is specified.

</td>
</tr>
<tr>
<td width="40%"><a id="CLFS_SCAN_BACKWARD"></a><a id="clfs_scan_backward"></a><dl>
<dt><b>CLFS_SCAN_BACKWARD</b></dt>
</dl>
</td>
<td width="60%">
Causes the next call to <b>ScanLogContainers</b> to proceed  in a backward direction. 

Cannot be used if <b>CLFS_SCAN_FORWARD</b> is specified.

</td>
</tr>
</table>

### -param pReserved [in, out, optional]

Reserved.  Set <i>pReserved</i> to <b>NULL</b>.

## -returns

If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

 The following  list identifies the possible error codes:

## -remarks

The ID of a log container is  returned in: <b>pcxScan-&gt;pinfoContainer-&gt;LogicalContainerId</b>.

<div class="alert"><b>Note</b>  The Common Log File System (CLFS) scan contexts are not thread-safe. They should not be used by more than one thread at a time, or passed into more than one asynchronous scan at a time.</div>
<div> </div>

#### Examples

For an example that uses this function, see <a href="/previous-versions/windows/desktop/clfs/enumerating-log-containers">Enumerating Log Containers</a>.

<div class="code"></div>

## -see-also

<a href="/windows/win32/api/clfs/ns-clfs-cls_scan_context~r1">CLFS_SCAN_CONTEXT</a>



<a href="/previous-versions/windows/desktop/clfs/clfs-scan-mode-constants">CLFS_SCAN_MODE</a>



<a href="/previous-versions/windows/desktop/clfs/common-log-file-system-functions">Common Log File System Functions</a>



<a href="/windows/desktop/api/clfsw32/nf-clfsw32-createlogcontainerscancontext">CreateLogContainerScanContext</a>



<a href="/windows/desktop/api/clfsw32/nf-clfsw32-getlogcontainername">GetLogContainerName</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a>