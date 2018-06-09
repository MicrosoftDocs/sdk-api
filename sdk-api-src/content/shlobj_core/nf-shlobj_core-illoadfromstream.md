---
UID: NF:shlobj_core.ILLoadFromStream
title: ILLoadFromStream function
author: windows-sdk-content
description: Deprecated. Loads an ITEMIDLIST structure from a stream.
old-location: shell\ILLoadFromStream.htm
old-project: shell
ms.assetid: 060cc008-eb6a-4359-b84b-05c26d69f793
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: ILLoadFromStream, ILLoadFromStream function [Windows Shell], _win32_ILLoadFromStream, shell.ILLoadFromStream, shlobj_core/ILLoadFromStream
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shlobj_core.h
req.include-header: Shlobj.h
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
tech.root: 
req.typenames: AUTOCOMPLETELISTOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
 - Windows.Storage.dll
api_name:
 - ILLoadFromStream
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# ILLoadFromStream function


## -description


<p class="CCE_Message">[This function is available through Windows XP Service Pack 2 (SP2) and Windows Server 2003. It might be altered or unavailable in subsequent versions of Windows.]

Deprecated. Loads an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure from a stream.


## -parameters




### -param pstm [in]

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>*</b>

A pointer that indicates the <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> interface that the <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> loads from.


### -param pidl [out]

Type: <b>PIDLIST_RELATIVE*</b>

Address of a pointer to an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure. <b>ILLoadFromStream</b> allocates the necessary memory for the structure, and assigns the address to this parameter.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM error-code otherwise.




## -remarks



When you are finished with the <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure, you must free it by calling <a href="https://msdn.microsoft.com/3457f36e-fdfd-44a4-90ca-a86f00bc9f36">ILFree</a>.




## -see-also




<a href="https://msdn.microsoft.com/40d5ce57-58dc-4c79-8fe6-5412e3d7dc64">ILSaveToStream</a>
 

 

