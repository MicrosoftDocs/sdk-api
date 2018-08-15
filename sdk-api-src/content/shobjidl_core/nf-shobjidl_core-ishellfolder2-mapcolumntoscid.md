---
UID: NF:shobjidl_core.IShellFolder2.MapColumnToSCID
title: IShellFolder2::MapColumnToSCID
author: windows-sdk-content
description: Converts a column to the appropriate property set ID (FMTID) and property ID (PID).
old-location: shell\IShellFolder2_MapColumnToSCID.htm
old-project: shell
ms.assetid: 4bd1f9a1-379b-4488-87d3-c7c7dc47c4d1
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IShellFolder2 interface [Windows Shell],MapColumnToSCID method, IShellFolder2.MapColumnToSCID, IShellFolder2::MapColumnToSCID, MapColumnToSCID, MapColumnToSCID method [Windows Shell], MapColumnToSCID method [Windows Shell],IShellFolder2 interface, _win32_IShellFolder2_MapColumnToSCID, shell.IShellFolder2_MapColumnToSCID, shobjidl_core/IShellFolder2::MapColumnToSCID
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.redist: 
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
 - IShellFolder2.MapColumnToSCID
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IShellFolder2::MapColumnToSCID


## -description


Converts a column to the appropriate property set ID (FMTID) and property ID (PID).


## -parameters




### -param iColumn [in]

Type: <b>UINT</b>

The column ID.


### -param pscid [out]

Type: <b><a href="https://msdn.microsoft.com/bf7b0e3b-527a-4ef5-894a-a7e1b7750e72">SHCOLUMNID</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/bf7b0e3b-527a-4ef5-894a-a7e1b7750e72">SHCOLUMNID</a> structure containing the FMTID and PID.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



