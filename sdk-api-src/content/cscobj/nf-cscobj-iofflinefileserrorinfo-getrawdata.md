---
UID: NF:cscobj.IOfflineFilesErrorInfo.GetRawData
title: IOfflineFilesErrorInfo::GetRawData
author: windows-sdk-content
description: Retrieves a block of bytes containing internal data associated with the error.
old-location: of\iofflinefileserrorinfo_getrawdata.htm
tech.root: OfflineFiles
ms.assetid: 70e5e444-7c46-4df9-8f77-da8dc331fcf0
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetRawData, GetRawData method [Offline Files], GetRawData method [Offline Files],IOfflineFilesErrorInfo interface, IOfflineFilesErrorInfo interface [Offline Files],GetRawData method, IOfflineFilesErrorInfo.GetRawData, IOfflineFilesErrorInfo::GetRawData, cscobj/IOfflineFilesErrorInfo::GetRawData, of.iofflinefileserrorinfo_getrawdata
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: cscobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
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
 - IOfflineFilesErrorInfo.GetRawData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- cscobj.h
: 
- IOfflineFilesErrorInfo.GetRawData
: 
---

# IOfflineFilesErrorInfo::GetRawData


## -description


Retrieves a block of bytes containing internal data associated with the error. The content of this block is intended for use by the Windows development and support teams and is subject to change in any version of Windows.  No definition of the data block is provided.


## -parameters




### -param ppBlob [out]

Receives the address of a BYTE_BLOB structure describing the raw data.  The caller must free this memory block by using the <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> function.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -remarks



The BYTE_BLOB structure is defined in Wtypes.h.




## -see-also




<a href="https://msdn.microsoft.com/6c78d475-aa63-49e4-863f-1a197801f2f9">IOfflineFilesErrorInfo</a>
 

 

