---
UID: NF:shobjidl_core.IFileSystemBindData2.SetJunctionCLSID
title: IFileSystemBindData2::SetJunctionCLSID
author: windows-sdk-content
description: Sets the class identifier (CLSID) of the object that implements IShellFolder, if the current item is a junction point.
old-location: shell\IFileSystemBindData2_SetJunctionCLSID.htm
old-project: shell
ms.assetid: e072818d-dfa4-4b95-93b6-275206596147
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IFileSystemBindData2 interface [Windows Shell],SetJunctionCLSID method, IFileSystemBindData2.SetJunctionCLSID, IFileSystemBindData2::SetJunctionCLSID, SetJunctionCLSID, SetJunctionCLSID method [Windows Shell], SetJunctionCLSID method [Windows Shell],IFileSystemBindData2 interface, _shell_IFileSystemBindData2_SetJunctionCLSID, shell.IFileSystemBindData2_SetJunctionCLSID, shobjidl_core/IFileSystemBindData2::SetJunctionCLSID
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - shobjidl_core.h
api_name:
 - IFileSystemBindData2.SetJunctionCLSID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFileSystemBindData2::SetJunctionCLSID


## -description


Sets the class identifier (CLSID) of the object that implements <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a>, if the current item is a junction point.


## -parameters




### -param clsid [in]

Type: <b>REFCLSID</b>

The CLSID for the object that implements <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a> with a junction point as its current item.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



