---
UID: NF:shlwapi.IStream_ReadPidl
title: IStream_ReadPidl function
author: windows-sdk-content
description: Reads a pointer to an item identifier list (PIDL) from an IStream object into a PIDLIST_RELATIVE object.
old-location: shell\IStream_ReadPidl.htm
tech.root: shell
ms.assetid: 63b1f842-139b-4558-8105-4986ce592b56
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: IStream_ReadPidl, IStream_ReadPidl function [Windows Shell], _shell_IStream_ReadPidl, shell.IStream_ReadPidl, shlwapi/IStream_ReadPidl
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shlwapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - API-MS-Win-shlwapi-Winrt-storage-l1-1-0.dll
 - api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
api_name:
 - IStream_ReadPidl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IStream_ReadPidl function


## -description


Reads a pointer to an item identifier list (PIDL) from an <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> object into a PIDLIST_RELATIVE object.


## -parameters




### -param pstm [in]

Type: <b>IStream*</b>

A pointer to the <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> from which the PIDL is read.


### -param ppidlOut [out]

Type: <b>PIDLIST_RELATIVE*</b>

A pointer to the resulting PIDL.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



