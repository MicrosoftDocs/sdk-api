---
UID: NF:imapi2fs.IFileSystemImage3.ProbeSpecificFileSystem
title: IFileSystemImage3::ProbeSpecificFileSystem
author: windows-sdk-content
description: Determines if a specific file system on the current media is appendable through the IMAPI.
old-location: imapi\ifilesystemimage3_probespecificfilesystem.htm
tech.root: imapi
ms.assetid: 0594c2e4-30ba-4d02-948e-09ec6a4ec352
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IFileSystemImage3 interface [IMAPI],ProbeSpecificFileSystem method, IFileSystemImage3.ProbeSpecificFileSystem, IFileSystemImage3::ProbeSpecificFileSystem, ProbeSpecificFileSystem, ProbeSpecificFileSystem method [IMAPI], ProbeSpecificFileSystem method [IMAPI],IFileSystemImage3 interface, imapi.ifilesystemimage3_probespecificfilesystem, imapi2fs/IFileSystemImage3::ProbeSpecificFileSystem
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: imapi2fs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2fs.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2fs.h
api_name:
 - IFileSystemImage3.ProbeSpecificFileSystem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileSystemImage3::ProbeSpecificFileSystem


## -description


Determines if a specific file system on the current media is appendable through the IMAPI.


## -parameters




### -param fileSystemToProbe [in]

The file system on the current media to probe.


### -param isAppendable [out, ref, retval]

A <b>VARIANT_BOOL</b> value specifying if the specified file system is appendable.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation.




## -remarks



This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the <a href="http://go.microsoft.com/fwlink/p/?linkid=141659">Windows Feature Pack for Storage</a>. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.




## -see-also




<a href="https://msdn.microsoft.com/ffe343fa-2837-41f7-b7e0-097788fb5d4e">IFileSystemImage3</a>
 

 

