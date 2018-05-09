---
UID: NF:shlobj_core.ILSaveToStream
title: ILSaveToStream function
author: windows-driver-content
description: Saves an ITEMIDLIST structure to a stream.
old-location: shell\ILSaveToStream.htm
old-project: shell
ms.assetid: 40d5ce57-58dc-4c79-8fe6-5412e3d7dc64
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: ILSaveToStream, ILSaveToStream function [Windows Shell], _win32_ILSaveToStream, shell.ILSaveToStream, shlobj_core/ILSaveToStream
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: AUTOCOMPLETELISTOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Shell32.dll
-	ext-ms-win-shell-shell32-l1-2-1.dll
-	Ext-MS-Win-Shell-Shell32-L1-2-2.dll
-	Windows.Storage.dll
api_name:
-	ILSaveToStream
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# ILSaveToStream function


## -description


Saves an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure to a stream.


## -parameters




### -param pstm [in]

Type: <b>IStream *</b>

A pointer to the <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> interface where the <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> is saved.


### -param pidl [in]

Type: <b>PCUIDLIST_RELATIVE</b>

A pointer to the <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure to be saved.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM error value otherwise.




## -remarks



The stream must be opened for writing, or <b>ILSaveToStream</b> returns an error.




## -see-also




<a href="https://msdn.microsoft.com/060cc008-eb6a-4359-b84b-05c26d69f793">ILLoadFromStream</a>
 

 

