---
UID: NF:clfsw32.AddLogContainer
title: AddLogContainer function (clfsw32.h)
description: Adds a container to the physical log that is associated with the log handle if the calling process has write access to the .blf file and the ability to create files in the target directory of the container.
helpviewer_keywords: ["AddLogContainer","AddLogContainer function [Files]","clfsw32/AddLogContainer","fs.addlogcontainer"]
old-location: fs\addlogcontainer.htm
tech.root: fs
ms.assetid: 5e886b96-9431-43f6-b888-e0f47c432371
ms.date: 12/05/2018
ms.keywords: AddLogContainer, AddLogContainer function [Files], clfsw32/AddLogContainer, fs.addlogcontainer
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
 - AddLogContainer
 - clfsw32/AddLogContainer
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
 - AddLogContainer
---

# AddLogContainer function


## -description

Adds a container to the physical log  that is associated with the log handle—if the calling process has  write access to the .blf file and the ability to create files in the target directory of the container.

This function is different from  <a href="/windows/desktop/api/clfsw32/nf-clfsw32-addlogcontainerset">AddLogContainerSet</a>, because it  adds only one  container.  To add multiple containers,  it is  more efficient to use <b>AddLogContainerSet</b>, which allows you to add more than one container. Adding containers allows a client to increase the size of a log.

## -parameters

### -param hLog [in]

The handle to an open log. 

The handle must  be   obtained from <a href="/windows/desktop/api/clfsw32/nf-clfsw32-createlogfile">CreateLogFile</a> with write access to the log. The client application must have  write access to the .blf file, and the ability to create files in the target directory of a container.

### -param pcbContainer [in, optional]

The optional parameter that specifies the size of the container, in bytes.  

The minimum size is  512 KB for normal logs and 1024 KB for multiplexed logs. The maximum size is approximately 4 gigabytes.

This parameter is required if the containers are being added to a newly created log.  If a container is already created, this parameter can  be <b>NULL</b>, or some value that is at least as large as the size of the first container. 


Log container sizes are multiples of the log region size  (512 KB).  When you add a container to a new file, the <b>AddLogContainer</b> function rounds the size of the container up to the next 512 KB boundary, and returns that size in the value pointed to by <i>pcbContainer</i>.  

Similarly,  if the log already has at least one container and the value of <i>*pcbContainer</i> is at least as large as the current container size, the function creates all containers with the current internal size and returns that size in <i>*pcbContainer</i>.

### -param pwszContainerPath [in]

A pointer to a null-terminated string that contains a valid path for the new container on a log volume.

### -param pReserved [in, out, optional]

Reserved.  Set <i>pReserved</i> to <b>NULL</b>.

## -returns

If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The following list identifies the possible error codes:

## -see-also

<a href="/windows/desktop/api/clfsw32/nf-clfsw32-addlogcontainerset">AddLogContainerSet</a>



<a href="/previous-versions/windows/desktop/clfs/common-log-file-system-functions">Common Log File System Functions</a>



<a href="/windows/desktop/api/clfsw32/nf-clfsw32-createlogfile">CreateLogFile</a>
