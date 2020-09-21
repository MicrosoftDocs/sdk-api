---
UID: NF:clfsw32.RemoveLogContainer
title: RemoveLogContainer function (clfsw32.h)
description: Removes one container from a log that is associated with a dedicated or multiplexed log handle.
helpviewer_keywords: ["RemoveLogContainer","RemoveLogContainer function [Files]","clfsw32/RemoveLogContainer","fs.removelogcontainer"]
old-location: fs\removelogcontainer.htm
tech.root: fs
ms.assetid: e6571cb0-8453-4db0-9a33-17339c4ea223
ms.date: 12/05/2018
ms.keywords: RemoveLogContainer, RemoveLogContainer function [Files], clfsw32/RemoveLogContainer, fs.removelogcontainer
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
 - RemoveLogContainer
 - clfsw32/RemoveLogContainer
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
 - RemoveLogContainer
---

# RemoveLogContainer function


## -description

Removes  one  container from a log that is associated with a dedicated or multiplexed log handle.

A client must have  administrative privileges on the log handle to  remove   a  container.   To remove multiple containers,  use the   <a href="/windows/desktop/api/clfsw32/nf-clfsw32-removelogcontainerset">RemoveLogContainerSet</a>  function.

## -parameters

### -param hLog [in]

A handle to the log that is obtained from <a href="/windows/desktop/api/clfsw32/nf-clfsw32-createlogfile">CreateLogFile</a>.

### -param pwszContainerPath [in]

A pointer to a wide character string that contains a  path for a  log container that is created by either  <a href="/windows/desktop/api/clfsw32/nf-clfsw32-addlogcontainer">AddLogContainer</a> or <a href="/windows/desktop/api/clfsw32/nf-clfsw32-addlogcontainerset">AddLogContainerSet</a>.

### -param fForce [in]

The deletion flag  that determines when and how a container is deleted.

If <i>fForce</i> is <b>TRUE</b>, and the container is part of the active log region, the container is not deleted and an error <b>ERROR_LOG_CANT_DELETE</b> is returned.

If <b>FALSE</b>, the container is deleted when the container is no longer a part of the active log region.

### -param pReserved [in, out, optional]

This parameter is reserved and should be  set to <b>NULL</b>.

## -returns

If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

 The following list identifies the possible error codes:

## -remarks

  By default, container deletion is lazy, which means that a container is deleted  only if it is not part of an active log.  If the container is part of the active log, it is marked for deletion. However,  deletion does not occur until the  end  of the log exceeds the last sector of the container, or the container has a logical identifier that is greater than the logical identifier of the head of the active log.  The log size reflects the container deletion only when the container is deleted physically.

A log client can request a forced deletion on a container by setting the deletion flag to <b>TRUE</b>. This has the same effect  as deleting a container  that  is  not part of the active log.  However, if the container is part of the active log, the call fails without marking the container for deletion.

## -see-also

<a href="/windows/desktop/api/clfsw32/nf-clfsw32-addlogcontainer">AddLogContainer</a>



<a href="/windows/desktop/api/clfsw32/nf-clfsw32-addlogcontainerset">AddLogContainerSet</a>



<a href="/previous-versions/windows/desktop/clfs/common-log-file-system-functions">Common Log File System Functions</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a>



<a href="/windows/desktop/api/clfsw32/nf-clfsw32-removelogcontainerset">RemoveLogContainerSet</a>