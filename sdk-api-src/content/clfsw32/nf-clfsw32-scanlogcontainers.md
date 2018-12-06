---
UID: NF:clfsw32.ScanLogContainers
title: ScanLogContainers function
author: windows-sdk-content
description: Enumerates log containers. Call this function repeatedly to iterate over all log containers.
old-location: fs\scanlogcontainers.htm
tech.root: Clfs
ms.assetid: a3a374ab-e5e9-47c0-9a62-d880823035b5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CLFS_SCAN_BACKWARD, CLFS_SCAN_CLOSE, CLFS_SCAN_FORWARD, CLFS_SCAN_INIT, ScanLogContainers, ScanLogContainers function [Files], clfsw32/ScanLogContainers, fs.scanlogcontainers
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Clfsw32.dll
api_name:
 - ScanLogContainers
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ScanLogContainers function


## -description


Enumerates log containers. Call this function repeatedly to iterate over all log containers.


## -parameters




### -param pcxScan [in, out]

A pointer to a client-allocated <a href="https://msdn.microsoft.com/716fa005-c801-4a5d-99f1-0babe64dc4a8">CLFS_SCAN_CONTEXT</a> structure  that  the <a href="https://msdn.microsoft.com/863e600c-3a7b-47b4-9cc3-dcee1bfcc66b">CreateLogContainerScanContext</a> function initializes. 


### -param eScanMode [in]

The mode  for  containers  to  be scanned.  

Containers can be scanned in any  of the following <a href="https://msdn.microsoft.com/64bb2113-aded-4a80-8f1a-1668ad05ae1e">CLFS_SCAN_MODE</a> modes.

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
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

 The following  list identifies the possible error codes:




## -remarks



The ID of a log container is  returned in: <b>pcxScan-&gt;pinfoContainer-&gt;LogicalContainerId</b>.

<div class="alert"><b>Note</b>  The Common Log File System (CLFS) scan contexts are not thread-safe. They should not be used by more than one thread at a time, or passed into more than one asynchronous scan at a time.</div>
<div> </div>

#### Examples

For an example that uses this function, see <a href="https://msdn.microsoft.com/dc7e204c-201d-4a84-9a87-576c73627f67">Enumerating Log Containers</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/716fa005-c801-4a5d-99f1-0babe64dc4a8">CLFS_SCAN_CONTEXT</a>



<a href="https://msdn.microsoft.com/64bb2113-aded-4a80-8f1a-1668ad05ae1e">CLFS_SCAN_MODE</a>



<a href="https://msdn.microsoft.com/a3059828-d291-493d-a4fe-13d06e49ed12">Common Log File System Functions</a>



<a href="https://msdn.microsoft.com/863e600c-3a7b-47b4-9cc3-dcee1bfcc66b">CreateLogContainerScanContext</a>



<a href="https://msdn.microsoft.com/4ff12544-797d-48b9-9c42-4bec059e6551">GetLogContainerName</a>



<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a>
 

 

