---
UID: NF:clfsw32.CreateLogContainerScanContext
title: CreateLogContainerScanContext function (clfsw32.h)
description: Creates a scan context to use with ScanLogContainers to enumerate all log containers that are associated with a log, and performs the first scan.
helpviewer_keywords: ["CLFS_SCAN_BACKWARD","CLFS_SCAN_FORWARD","CLFS_SCAN_INIT","CreateLogContainerScanContext","CreateLogContainerScanContext function [Files]","clfsw32/CreateLogContainerScanContext","fs.createlogcontainerscancontext"]
old-location: fs\createlogcontainerscancontext.htm
tech.root: fs
ms.assetid: 863e600c-3a7b-47b4-9cc3-dcee1bfcc66b
ms.date: 12/05/2018
ms.keywords: CLFS_SCAN_BACKWARD, CLFS_SCAN_FORWARD, CLFS_SCAN_INIT, CreateLogContainerScanContext, CreateLogContainerScanContext function [Files], clfsw32/CreateLogContainerScanContext, fs.createlogcontainerscancontext
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
 - CreateLogContainerScanContext
 - clfsw32/CreateLogContainerScanContext
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
 - CreateLogContainerScanContext
---

# CreateLogContainerScanContext function


## -description

Creates a scan context to use with <a href="/windows/desktop/api/clfsw32/nf-clfsw32-scanlogcontainers">ScanLogContainers</a> to enumerate all log containers that are associated with a  log, and performs the first scan.

## -parameters

### -param hLog [in]

A  handle to the log that is obtained from <a href="/windows/desktop/api/clfsw32/nf-clfsw32-createlogfile">CreateLogFile</a> with permissions  to scan the log containers.  

The file can be  a dedicated or multiplexed log.

### -param cFromContainer [in]

The container where  the scan is to be started.  

This parameter is an ordinal number relative to the number of containers in the log.

### -param cContainers [in]

The number of <a href="/windows/desktop/api/clfs/ns-clfs-cls_container_information">CLFS_CONTAINER_INFORMATION</a> structures for  <b>CreateLogContainerScanContext</b> to allocate. 

This number is the number of containers scanned with each scan call so the caller knows the scan is complete when the number of containers returned is less than this value.

On exit, a pointer to the system-allocated array of <a href="/windows/desktop/api/clfs/ns-clfs-cls_container_information">CLFS_CONTAINER_INFORMATION</a> structures is placed in the <b>pinfoContainer</b> member of the client-allocated <a href="/windows/win32/api/clfs/ns-clfs-cls_scan_context~r1">CLFS_SCAN_CONTEXT</a> structure. This member is   pointed to by the <i>pcxScan</i> parameter (that is, "pcxScan-&gt;pinfoContainer[]"), and the actual number of structures in the array is placed in "pcxScan-&gt;cContainersReturned".

The client must call <a href="/windows/desktop/api/clfsw32/nf-clfsw32-scanlogcontainers">ScanLogContainers</a> with the <i>eScanMode</i> parameter set to <b>CLFS_SCAN_CLOSE</b>  so that it can free this array; otherwise, memory leaks result.

### -param eScanMode [in]

The mode to scan containers.  

Containers can be scanned in any one of the following modes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CLFS_SCAN_INIT__"></a><a id="clfs_scan_init__"></a><dl>
<dt><b>CLFS_SCAN_INIT  </b></dt>
</dl>
</td>
<td width="60%">
Initializes or reinitializes a scan from the first container in the container list.  

This mode initializes the container context and returns the first set of container descriptors  that  <i>cContainers</i> specifies.

</td>
</tr>
<tr>
<td width="40%"><a id="CLFS_SCAN_FORWARD"></a><a id="clfs_scan_forward"></a><dl>
<dt><b>CLFS_SCAN_FORWARD</b></dt>
</dl>
</td>
<td width="60%">
 Returns the first set of containers  that  <i>cContainers</i> specifies.

</td>
</tr>
<tr>
<td width="40%"><a id="CLFS_SCAN_BACKWARD"></a><a id="clfs_scan_backward"></a><dl>
<dt><b>CLFS_SCAN_BACKWARD</b></dt>
</dl>
</td>
<td width="60%">
 Returns the last set of containers  that <i>cContainers</i> specifies.

</td>
</tr>
</table>

### -param pcxScan [in, out]

A pointer to a client-allocated <a href="/windows/win32/api/clfs/ns-clfs-cls_scan_context~r1">CLFS_SCAN_CONTEXT</a> structure that receives a scan context that can be passed to the <a href="/windows/desktop/api/clfsw32/nf-clfsw32-scanlogcontainers">ScanLogContainers</a> function when a client scans the log containers of a dedicated log.

### -param pOverlapped [in, out, optional]

A pointer to an <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure that is required for asynchronous operation. 

This parameter can be <b>NULL</b> if an asynchronous operation is not used.

## -returns

If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The following list identifies the possible error codes:

## -remarks

After completing a scan, the client must call <a href="/windows/desktop/api/clfsw32/nf-clfsw32-scanlogcontainers">ScanLogContainers</a> again with the <i>eScanMode</i> parameter set to <b>CLFS_SCAN_CLOSE</b>  so that it can free the system-allocated array of <a href="/windows/desktop/api/clfs/ns-clfs-cls_container_information">CLFS_CONTAINER_INFORMATION</a> structures; otherwise, memory leaks result.


#### Examples

For an example that uses this function, see <a href="/previous-versions/windows/desktop/clfs/enumerating-log-containers">Enumerating Log Containers</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/clfs/ns-clfs-cls_container_information">CLFS_CONTAINER_INFORMATION</a>



<a href="/windows/win32/api/clfs/ns-clfs-cls_scan_context~r1">CLFS_SCAN_CONTEXT</a>



<a href="/previous-versions/windows/desktop/clfs/clfs-scan-mode-constants">CLFS_SCAN_MODE</a>



<a href="/previous-versions/windows/desktop/clfs/common-log-file-system-functions">Common Log File System Functions</a>



<a href="/windows/desktop/api/clfsw32/nf-clfsw32-scanlogcontainers">ScanLogContainers</a>