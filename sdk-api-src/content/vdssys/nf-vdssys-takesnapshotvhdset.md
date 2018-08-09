---
UID: NF:vdssys.TakeSnapshotVhdSet
title: TakeSnapshotVhdSet function
author: windows-sdk-content
description: Creates a snapshot of the current virtual disk for VHD Set files.
old-location: vhd\takesnapshotvhdset.htm
old-project: VStor
ms.assetid: 370C6DB2-EA0F-4B6F-BA14-CE14377E2314
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: TakeSnapshotVhdSet, TakeSnapshotVhdSet function [VHD], vdssys/TakeSnapshotVhdSet, vhd.takesnapshotvhdset, virtdisk/TakeSnapshotVhdSet
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: vdssys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - TakeSnapshotVhdSet
product: Windows
targetos: Windows
req.lib: VirtDisk.lib
req.dll: VirtDisk.dll
req.irql: 
req.product: Windows UI
---

# TakeSnapshotVhdSet function


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Creates a snapshot of the current virtual disk for VHD Set files.


## -parameters




### -param VirtualDiskHandle [in]

A handle to the open virtual disk. This must be a VHD Set file.


### -param Parameters [in]

A pointer to a valid <a href="https://msdn.microsoft.com/39D7287B-FA5E-4584-8E0A-69A857736D02">TAKE_SNAPSHOT_VHDSET_PARAMETERS</a> structure that contains snapshot data.


### -param Flags [in]

Snapshot flags, which must be a valid combination of the <a href="https://msdn.microsoft.com/2A714FFB-E462-418E-B0AC-E7929619604B">TAKE_SNAPSHOT_VHDSET_FLAG</a> enumeration


## -returns



Status of the request.

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is an error code. For more information, see 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.



