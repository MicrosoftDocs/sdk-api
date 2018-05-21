---
UID: NF:shobjidl_core.IFileSystemBindData2.GetJunctionCLSID
title: IFileSystemBindData2::GetJunctionCLSID
author: windows-driver-content
description: Gets the class identifier (CLSID) of the object that implements IShellFolder for the item, if the item is a junction point.
old-location: shell\IFileSystemBindData2_GetJunctionCLSID.htm
old-project: shell
ms.assetid: 57c5205a-9a56-4c47-bec4-11a690107bc6
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: GetJunctionCLSID, GetJunctionCLSID method [Windows Shell], GetJunctionCLSID method [Windows Shell],IFileSystemBindData2 interface, IFileSystemBindData2 interface [Windows Shell],GetJunctionCLSID method, IFileSystemBindData2.GetJunctionCLSID, IFileSystemBindData2::GetJunctionCLSID, _shell_IFileSystemBindData2_GetJunctionCLSID, shell.IFileSystemBindData2_GetJunctionCLSID, shobjidl_core/IFileSystemBindData2::GetJunctionCLSID
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	shobjidl_core.h
api_name:
-	IFileSystemBindData2.GetJunctionCLSID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFileSystemBindData2::GetJunctionCLSID


## -description


Gets the class identifier (CLSID) of the object that implements <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a> for the item, if the item is a junction point.


## -parameters




### -param pclsid [out]

Type: <b>CLSID*</b>

When this method returns successfully, receives a pointer to the CLSID of the object that implements <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a> for the current item, if the item is a junction point.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



