---
UID: NF:virtdisk.SetVirtualDiskMetadata
title: SetVirtualDiskMetadata function
author: windows-sdk-content
description: Sets a metadata item for a virtual disk.
old-location: vstor\setvirtualdiskmetadata.htm
old-project: VStor
ms.assetid: 27ee1529-ccd9-43ea-aed9-4fd32d793354
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: SetVirtualDiskMetadata, SetVirtualDiskMetadata function [Virtual Storage], virtdisk/SetVirtualDiskMetadata, vstor.setvirtualdiskmetadata
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: virtdisk.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: VIRTUAL_DISK_ACCESS_MASK
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - VirtDisk.dll
api_name:
 - SetVirtualDiskMetadata
product: Windows
targetos: Windows
req.lib: VirtDisk.lib
req.dll: VirtDisk.dll
req.irql: 
req.product: Windows UI
---

# SetVirtualDiskMetadata function


## -description


Sets a metadata item for a virtual disk.


## -parameters




### -param VirtualDiskHandle [in]

Handle to an open virtual disk.


### -param Item [in]

Address of a <b>GUID</b> identifying the metadata to retrieve.


### -param MetaDataSize [in]

Address of a <b>ULONG</b> containing the size, in bytes, of 
      the buffer pointed to by the <i>MetaData</i> parameter.


### -param MetaData [in]

Address of the buffer containing the metadata to be stored.


## -returns



Status of the request.

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is an error code. For more information, see 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/79c3b3ad-4eaf-49ce-a8ee-b26faf6c2cba">VHD Functions</a>
 

 

