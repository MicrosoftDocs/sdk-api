---
UID: NF:shobjidl_core.IShellLinkDataList.CopyDataBlock
title: IShellLinkDataList::CopyDataBlock
author: windows-sdk-content
description: Retrieves a copy of a link's data block.
old-location: shell\IShellLinkDataList_CopyDataBlock.htm
tech.root: shell
ms.assetid: e02fb4c3-faec-40cc-ab97-d05cdcc148ed
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: CopyDataBlock, CopyDataBlock method [Windows Shell], CopyDataBlock method [Windows Shell],IShellLinkDataList interface, IShellLinkDataList interface [Windows Shell],CopyDataBlock method, IShellLinkDataList.CopyDataBlock, IShellLinkDataList::CopyDataBlock, _win32_IShellLinkDataList_CopyDataBlock, shell.IShellLinkDataList_CopyDataBlock, shobjidl_core/IShellLinkDataList::CopyDataBlock
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
 - IShellLinkDataList.CopyDataBlock
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellLinkDataList::CopyDataBlock


## -description


Retrieves a copy of a link's data block.


## -parameters




### -param dwSig [in]

Type: <b>DWORD</b>

The data block's signature. The signature value for a particular type of data block can be found in its structure reference. For a list of supported data block types and their associated structures, see <a href="https://msdn.microsoft.com/ac3279ad-1413-48bf-a830-4ec128352573">IShellLinkDataList</a>.


### -param ppDataBlock [out]

Type: <b>VOID**</b>

The address of a pointer to a copy of the data block structure. If <b>IShellLinkDataList::CopyDataBlock</b> returns a successful result, the calling application must free the memory when it is no longer needed by calling <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a>.


## -returns



Type: <b>HRESULT</b>

Returns <b>S_OK</b> if successful, or a COM error code otherwise.




## -see-also




<a href="https://msdn.microsoft.com/ac3279ad-1413-48bf-a830-4ec128352573">IShellLinkDataList</a>
 

 

