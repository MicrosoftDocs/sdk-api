---
UID: NS:clfs._CLS_SCAN_CONTEXT~r1
title: CLS_SCAN_CONTEXT
description: The CLS_SCAN_CONTEXT structure contains information about the containers that are being scanned by ScanLogContainers.
ms.date: 08/01/2022
ms.keywords: _CLS_SCAN_CONTEXT, CLS_SCAN_CONTEXT
targetos: Windows
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: clfs.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.typenames: CLS_SCAN_CONTEXT, *PCLS_SCAN_CONTEXT, PPCLS_SCAN_CONTEXT
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - _CLS_SCAN_CONTEXT
 - clfs/_CLS_SCAN_CONTEXT
 - PCLS_SCAN_CONTEXT
 - clfs/PCLS_SCAN_CONTEXT
 - CLS_SCAN_CONTEXT
 - clfs/CLS_SCAN_CONTEXT
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - clfs.h
api_name:
 - _CLS_SCAN_CONTEXT
 - CLS_SCAN_CONTEXT
---

# CLS_SCAN_CONTEXT structure


## -description

Contains information about the containers that are being scanned by <a href="/windows/desktop/api/clfsw32/nf-clfsw32-scanlogcontainers">ScanLogContainers</a>, the kind of scan that is being performed, and a  cursor to track which containers have been scanned.

## -struct-fields

### -field cidNode

The ID of the current node. For more information, see <a href="/windows/desktop/api/clfs/ns-clfs-clfs_node_id">CLFS_NODE_ID</a>.

### -field hLog

A handle to the log being scanned that is obtained from <a href="/windows/desktop/api/clfsw32/nf-clfsw32-createlogfile">CreateLogFile</a> with permissions  to scan the log containers.

### -field cIndex

The index of the current container.

### -field cContainers

The number of system-allocated <a href="/windows/desktop/api/clfs/ns-clfs-cls_container_information">CLFS_CONTAINER_INFORMATION</a> structures in an array that is pointed to by <b>pinfoContainer</b>. 

That is, this member is the number of containers to scan with each scan call.   The caller knows the scan is complete when the number of containers returned is less than this value.

### -field cContainersReturned

The number of containers that are returned after a call to <a href="/windows/desktop/api/clfsw32/nf-clfsw32-scanlogcontainers">ScanLogContainers</a>.

### -field eScanMode

The mode in which containers are scanned.  

Containers can be scanned in one of the following modes.

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
Initializes the scan context, but does not allocate associated storage.  

The initialization is destructive, because all  data that is stored in the current scan context is lost.

</td>
</tr>
<tr>
<td width="40%"><a id="CLFS_SCAN_CLOSE"></a><a id="clfs_scan_close"></a><dl>
<dt><b>CLFS_SCAN_CLOSE</b></dt>
</dl>
</td>
<td width="60%">
Uninitializes the scan context and deallocates  system storage that is associated with a scan context.

</td>
</tr>
<tr>
<td width="40%"><a id="CLFS_SCAN_FORWARD"></a><a id="clfs_scan_forward"></a><dl>
<dt><b>CLFS_SCAN_FORWARD</b></dt>
</dl>
</td>
<td width="60%">
Causes the next call to <a href="/windows/desktop/api/clfsw32/nf-clfsw32-scanlogcontainers">ScanLogContainers</a> to proceed  in a forward direction. 

Cannot be used if <b>CLFS_SCAN_BACKWARD</b> is specified.

</td>
</tr>
<tr>
<td width="40%"><a id="CLFS_SCAN_BACKWARD"></a><a id="clfs_scan_backward"></a><dl>
<dt><b>CLFS_SCAN_BACKWARD</b></dt>
</dl>
</td>
<td width="60%">
Causes the next call to <a href="/windows/desktop/api/clfsw32/nf-clfsw32-scanlogcontainers">ScanLogContainers</a> to proceed  in a backward direction. 

Cannot be used if <b>CLFS_SCAN_FORWARD</b> is specified.

</td>
</tr>
</table>

### -field pinfoContainer

A pointer to
					a client-allocated array of <a href="/windows/desktop/api/clfs/ns-clfs-cls_container_information">CLFS_CONTAINER_INFORMATION</a> structures to be filled by <a href="/windows/desktop/api/clfsw32/nf-clfsw32-scanlogcontainers">ScanLogContainers</a> after each successful call.

## -remarks

This structure is allocated by the client, initialized using <a href="/windows/desktop/api/clfsw32/nf-clfsw32-createlogcontainerscancontext">CreateLogContainerScanContext</a>, and then passed to <a href="/windows/desktop/api/clfsw32/nf-clfsw32-scanlogcontainers">ScanLogContainers</a> in repeated calls.

## -see-also

<a href="/windows/desktop/api/clfs/ns-clfs-cls_container_information">CLFS_CONTAINER_INFORMATION</a>



<a href="/windows/desktop/api/clfs/ns-clfs-clfs_node_id">CLFS_NODE_ID</a>



<a href="/windows/desktop/api/clfsw32/nf-clfsw32-scanlogcontainers">ScanLogContainers</a>
