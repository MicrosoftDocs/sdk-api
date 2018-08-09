---
UID: NF:vdssys.ModifyVhdSet
title: ModifyVhdSet function
author: windows-sdk-content
description: Modifies the internal contents of a virtual disk file. Can be used to set the active leaf, or to fix up snapshot entries.
old-location: vhd\modifyvhdset.htm
old-project: VStor
ms.assetid: C0BDAF45-8F87-4EF5-81F3-F15E7E575EA1
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ModifyVhdSet, ModifyVhdSet function [VHD], vdssys/ModifyVhdSet, vhd.modifyvhdset, virtdisk/ModifyVhdSet
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
 - ModifyVhdSet
product: Windows
targetos: Windows
req.lib: VirtDisk.lib
req.dll: VirtDisk.dll
req.irql: 
req.product: Windows UI
---

# ModifyVhdSet function


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Modifies the internal contents of a virtual disk file. Can be used to set the active leaf, or to fix up snapshot entries.


## -parameters




### -param VirtualDiskHandle

TBD


### -param Parameters [in]

A pointer to a valid <a href="https://msdn.microsoft.com/558323D6-2D97-40C8-9CAF-E97604D2F742">MODIFY_VHDSET_PARAMETERS</a> structure that contains modification data.


### -param Flags [in]

A handle to the open virtual disk. This must be a VHD Set file.

Modification flags, which must be a valid combination of the <a href="https://msdn.microsoft.com/E983A928-CE3A-4B68-BDB5-CC21CB2BCC6F">MODIFY_VHDSET_FLAG</a> enumeration.


## -returns



Status of the request.

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is an error code. For more information, see 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.



