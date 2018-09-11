---
UID: NF:shlobj.SHCreateQueryCancelAutoPlayMoniker
title: SHCreateQueryCancelAutoPlayMoniker function
author: windows-sdk-content
description: Deprecated. Creates a QueryCancelAutoPlay class moniker, which can then be used to register the IQueryCancelAutoPlay handler in the running object table (ROT).
old-location: shell\SHCreateQueryCancelAutoPlayMoniker.htm
tech.root: shell
ms.assetid: 560a2b30-66f4-4b0f-9d46-ae714491c376
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: SHCreateQueryCancelAutoPlayMoniker, SHCreateQueryCancelAutoPlayMoniker function [Windows Shell], _shell_SHCreateQueryCancelAutoPlayMoniker, shell.SHCreateQueryCancelAutoPlayMoniker, shlobj/SHCreateQueryCancelAutoPlayMoniker
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHCreateQueryCancelAutoPlayMoniker
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SHCreateQueryCancelAutoPlayMoniker function


## -description


<p class="CCE_Message">[This function is deprecated. Use <a href="https://msdn.microsoft.com/9361b2c1-ef26-4225-92ff-e0bef0285bc4">CreateClassMoniker</a> instead. Note that the CLSID used in the call to <b>CreateClassMoniker</b> must be application-defined. Do not call <b>CreateClassMoniker</b> with a system-defined CLSID.]

Deprecated. Creates a <b>QueryCancelAutoPlay</b> class moniker, which can then be used to register the <a href="https://msdn.microsoft.com/7dd470cd-163b-43e1-80d9-cdaa8b615858">IQueryCancelAutoPlay</a> handler in the running object table (ROT).


## -parameters




### -param ppmoniker [out]

Type: <b><a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a>**</b>

The address of a <a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a> interface pointer that, when this function returns successfully, receives the <b>QueryCancelAutoPlay</b> class moniker. If this function call fails, this value is <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If successful, <b>SHCreateQueryCancelAutoPlayMoniker</b> calls the interface's <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a> method and increments the reference count. When you are finished, call the interface's <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> method to release.




## -see-also




<a href="https://msdn.microsoft.com/9361b2c1-ef26-4225-92ff-e0bef0285bc4">CreateClassMoniker</a>
 

 

