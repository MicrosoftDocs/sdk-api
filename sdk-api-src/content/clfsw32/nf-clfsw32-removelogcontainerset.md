---
UID: NF:clfsw32.RemoveLogContainerSet
title: RemoveLogContainerSet function (clfsw32.h)
description: Removes multiple containers from a log that is associated with a dedicated or multiplexed log handle.
helpviewer_keywords: ["RemoveLogContainerSet","RemoveLogContainerSet function [Files]","clfsw32/RemoveLogContainerSet","fs.removelogcontainerset"]
old-location: fs\removelogcontainerset.htm
tech.root: fs
ms.assetid: adc35813-7368-4d8c-ad2b-1bb0824ad019
ms.date: 12/05/2018
ms.keywords: RemoveLogContainerSet, RemoveLogContainerSet function [Files], clfsw32/RemoveLogContainerSet, fs.removelogcontainerset
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
 - RemoveLogContainerSet
 - clfsw32/RemoveLogContainerSet
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
 - RemoveLogContainerSet
---

# RemoveLogContainerSet function


## -description

Removes multiple containers from a log that is associated with a dedicated or multiplexed log handle.

A client must have  administrative privileges on the log handle to  remove a container. The <a href="/windows/desktop/api/clfsw32/nf-clfsw32-removelogcontainer">RemoveLogContainer</a> function is a special case of this <b>RemoveLogContainerSet</b> function, because it removes only one container.  To remove multiple containers, use the <b>RemoveLogContainerSet</b>.

## -parameters

### -param hLog [in]

A handle to the log that is obtained from <a href="/windows/desktop/api/clfsw32/nf-clfsw32-createlogfile">CreateLogFile</a>.  

The log handle must have administrative permission to add a log container, and can refer to either a dedicated or multiplexed log.

### -param cContainer [in]

The number of container path names in an array that is pointed to by <i>rgwszContainerPath</i>.  

This value must be nonzero.

### -param rgwszContainerPath [in]

An array of pointers to container path names that contain  <i>cContainers</i> pointers.  

Each path name is a wide character string that identifies  a container  created by either <a href="/windows/desktop/api/clfsw32/nf-clfsw32-addlogcontainer">AddLogContainer</a> or <a href="/windows/desktop/api/clfsw32/nf-clfsw32-addlogcontainerset">AddLogContainerSet</a>.

### -param fForce [in]

The deletion flag  that determines when and how a container is deleted.

If <i>fForce</i> is <b>TRUE</b>, and the container is part of the active log region, the container is not deleted and an error <b>ERROR_LOG_CANT_DELETE</b> is returned.

If <b>FALSE</b>, the container is deleted when the container is no longer a part of the active log region.

### -param pReserved [in, out, optional]

Reserved.  Set <i>pReserved</i> to <b>NULL</b>.

## -returns

If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The following list identifies the  possible error codes:

## -remarks

By default, container deletion is lazy, which means that a container is deleted  only if it is  not part of the active log.  If the container is part of the active log it is marked for deletion. This deletion is deferred until the tail of the log exceeds the last sector of the container, or the container has a logical identifier that is greater than the logical identifier of the head of the active log.  The log size reflects the container deletion only when the container is  deleted physically.


A log client can request a forced deletion on a container by setting the deletion flag to <b>TRUE</b>. This has the same effect  as  deleting a container that  is  not part of the active log.  However, if a container is part of the active log, the call fails without marking the container for deletion.

## -see-also

<a href="/windows/desktop/api/clfsw32/nf-clfsw32-addlogcontainer">AddLogContainer</a>



<a href="/windows/desktop/api/clfsw32/nf-clfsw32-addlogcontainerset">AddLogContainerSet</a>



<a href="/previous-versions/windows/desktop/clfs/common-log-file-system-functions">Common Log File System Functions</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a>



<a href="/windows/desktop/api/clfsw32/nf-clfsw32-removelogcontainer">RemoveLogContainer</a>