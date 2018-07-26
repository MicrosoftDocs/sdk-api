---
UID: NF:shobjidl_core.IShellLinkDataList.RemoveDataBlock
title: IShellLinkDataList::RemoveDataBlock
author: windows-sdk-content
description: Removes a data block from a link.
old-location: shell\IShellLinkDataList_RemoveDataBlock.htm
old-project: shell
ms.assetid: 32660c95-4b09-4ede-b02d-bf3a335a9097
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: IShellLinkDataList interface [Windows Shell],RemoveDataBlock method, IShellLinkDataList.RemoveDataBlock, IShellLinkDataList::RemoveDataBlock, RemoveDataBlock, RemoveDataBlock method [Windows Shell], RemoveDataBlock method [Windows Shell],IShellLinkDataList interface, _win32_IShellLinkDataList_RemoveDataBlock, shell.IShellLinkDataList_RemoveDataBlock, shobjidl_core/IShellLinkDataList::RemoveDataBlock
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellLinkDataList.RemoveDataBlock
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IShellLinkDataList::RemoveDataBlock


## -description


Removes a data block from a link.


## -parameters




### -param dwSig [in]

Type: <b>DWORD</b>

The data block's signature. The signature value for a particular type of data block can be found in its structure reference. For a list of supported data block types and their associated structures, see <a href="https://msdn.microsoft.com/ac3279ad-1413-48bf-a830-4ec128352573">IShellLinkDataList</a>.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM error code otherwise.




## -see-also




<a href="https://msdn.microsoft.com/ac3279ad-1413-48bf-a830-4ec128352573">IShellLinkDataList</a>
 

 

