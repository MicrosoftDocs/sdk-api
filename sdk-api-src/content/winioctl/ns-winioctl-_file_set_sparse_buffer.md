---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _FILE_SET_SPARSE_BUFFER structure


## -description


Specifies the sparse state to be set.<b>Windows Server 2003 and Windows XP:  </b>This structure is optional. For more information, see 
      <a href="https://msdn.microsoft.com/aa8f5880-f831-49b6-8359-fe07c78c032f">FSCTL_SET_SPARSE</a>.




## -struct-fields




### -field SetSparse

If <b>TRUE</b>, makes the file sparse.

If <b>FALSE</b>, makes the file not sparse.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:  </b>A value of <b>FALSE</b> for this member is valid only on files that no longer have any 
        sparse regions. For more information, see 
        <a href="https://msdn.microsoft.com/aa8f5880-f831-49b6-8359-fe07c78c032f">FSCTL_SET_SPARSE</a>.

<b>Windows Server 2003 and Windows XP:  </b>A value of <b>FALSE</b> for this member is not supported. Specifying 
        <b>FALSE</b> will cause the 
        <a href="https://msdn.microsoft.com/aa8f5880-f831-49b6-8359-fe07c78c032f">FSCTL_SET_SPARSE</a> call to fail.


## -see-also




<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/aa8f5880-f831-49b6-8359-fe07c78c032f">FSCTL_SET_SPARSE</a>
 

 

