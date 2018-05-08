---
UID: NF:virtdisk.ApplySnapshotVhdSet
title: ApplySnapshotVhdSet function
author: windows-driver-content
description: Applies a snapshot of the current virtual disk for VHD Set files.
old-location: vhd\applysnapshotvhdset.htm
old-project: VStor
ms.assetid: 1194B20E-AA50-4AEC-B9C4-AEA1BA84DD99
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: ApplySnapshotVhdSet, ApplySnapshotVhdSet function [VHD], vhd.applysnapshotvhdset, virtdisk/ApplySnapshotVhdSet
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: virtdisk.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VIRTUAL_DISK_ACCESS_MASK
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	VirtDisk.dll
api_name:
-	ApplySnapshotVhdSet
product: Windows
targetos: Windows
req.lib: VirtDisk.lib
req.dll: VirtDisk.dll
req.irql: 
req.product: Windows UI
---

# ApplySnapshotVhdSet function


## -description


Applies a snapshot of the current virtual disk for VHD Set files.


## -parameters




### -param VirtualDiskHandle [in]

A handle to an open virtual disk. For information on how to open a virtual disk, see the 
      <a href="https://msdn.microsoft.com/08e2a82d-9110-42b1-be09-dc5150da42f6">OpenVirtualDisk</a> function.


### -param Parameters [in]

A pointer to a valid <a href="https://msdn.microsoft.com/0C3A8097-0630-412E-AF23-144E3D98D292">APPLY_SNAPSHOT_VHDSET_PARAMETERS</a> structure that contains snapshot data.


### -param Flags [in]

A valid combination of values of the 
      <a href="https://msdn.microsoft.com/96ED6EB4-BB11-430D-9B2E-C905C223D261">APPLY_SNAPSHOT_VHDSET_FLAG</a> enumeration.


## -returns



Status of the request.

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is an error code. For more information, see 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/79c3b3ad-4eaf-49ce-a8ee-b26faf6c2cba">VHD Functions</a>
 

 

