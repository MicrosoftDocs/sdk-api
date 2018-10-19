---
UID: NF:shobjidl_core.IShellLinkDataList.AddDataBlock
title: IShellLinkDataList::AddDataBlock
author: windows-sdk-content
description: Adds a data block to a link.
old-location: shell\IShellLinkDataList_AddDataBlock.htm
tech.root: shell
ms.assetid: 6580736f-e217-4e3e-9b6e-1c1c004916f4
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: AddDataBlock, AddDataBlock method [Windows Shell], AddDataBlock method [Windows Shell],IShellLinkDataList interface, IShellLinkDataList interface [Windows Shell],AddDataBlock method, IShellLinkDataList.AddDataBlock, IShellLinkDataList::AddDataBlock, _win32_IShellLinkDataList_AddDataBlock, shell.IShellLinkDataList_AddDataBlock, shobjidl_core/IShellLinkDataList::AddDataBlock
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellLinkDataList.AddDataBlock
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellLinkDataList::AddDataBlock


## -description


Adds a data block to a link.


## -parameters




### -param pDataBlock [in]

Type: <b>VOID*</b>

The data block structure. For a list of supported structures, see <a href="https://msdn.microsoft.com/ac3279ad-1413-48bf-a830-4ec128352573">IShellLinkDataList</a>.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM error code otherwise.




## -see-also




<a href="https://msdn.microsoft.com/ac3279ad-1413-48bf-a830-4ec128352573">IShellLinkDataList</a>
 

 

