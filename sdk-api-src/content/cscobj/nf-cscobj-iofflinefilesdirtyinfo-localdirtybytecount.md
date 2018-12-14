---
UID: NF:cscobj.IOfflineFilesDirtyInfo.LocalDirtyByteCount
title: IOfflineFilesDirtyInfo::LocalDirtyByteCount
author: windows-sdk-content
description: Retrieves the amount of unsynchronized (&#0034;dirty&#0034;) data for the associated file in the local Offline Files cache.
old-location: of\iofflinefilesdirtyinfo_localdirtybytecount.htm
tech.root: offlinefiles
ms.assetid: c261d5ac-5834-42c7-b644-4244db9d653e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IOfflineFilesDirtyInfo interface [Offline Files],LocalDirtyByteCount method, IOfflineFilesDirtyInfo.LocalDirtyByteCount, IOfflineFilesDirtyInfo::LocalDirtyByteCount, LocalDirtyByteCount, LocalDirtyByteCount method [Offline Files], LocalDirtyByteCount method [Offline Files],IOfflineFilesDirtyInfo interface, cscobj/IOfflineFilesDirtyInfo::LocalDirtyByteCount, of.iofflinefilesdirtyinfo_localdirtybytecount
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: cscobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IOfflineFilesDirtyInfo.LocalDirtyByteCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOfflineFilesDirtyInfo::LocalDirtyByteCount


## -description


Retrieves the amount of unsynchronized ("dirty") data for the associated file in the local Offline Files cache.


## -parameters




### -param pDirtyByteCount [out]

The number of bytes of unsynchronized data.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -remarks



This method can be called only for file items, which are represented by <a href="https://msdn.microsoft.com/53b9af4b-7526-4b54-bae2-61c97aa67ebf">IOfflineFilesFileItem</a> objects.




## -see-also




<a href="https://msdn.microsoft.com/10414443-9e7f-4520-80dd-d2ad098c1d44">IOfflineFilesDirtyInfo</a>
 

 

