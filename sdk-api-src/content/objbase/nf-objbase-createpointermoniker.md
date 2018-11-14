---
UID: NF:objbase.CreatePointerMoniker
title: CreatePointerMoniker function
author: windows-sdk-content
description: Creates a pointer moniker based on a pointer to an object.
old-location: com\createpointermoniker.htm
tech.root: com
ms.assetid: d4d40fd5-6035-4ddc-a443-01d32dcf4bca
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: CreatePointerMoniker, CreatePointerMoniker function [COM], _com_CreatePointerMoniker, com.createpointermoniker, objbase/CreatePointerMoniker
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: objbase.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - Ext-MS-Win-COM-OLE32-l1-1-0.dll
 - Ext-MS-Win-COM-OLE32-l1-1-1.dll
 - Ext-MS-Win-COM-OLE32-l1-1-2.dll
 - ext-ms-win-com-ole32-l1-1-3.dll
 - Ext-MS-Win-Com-Ole32-L1-1-4.dll
api_name:
 - CreatePointerMoniker
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- CreatePointerMoniker
: 
---

# CreatePointerMoniker function


## -description


Creates a pointer moniker based on a pointer to an object.


## -parameters




### -param punk [in, optional]

A pointer to an <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface on the object to be identified by the resulting moniker.


### -param ppmk [out]

The address of an <a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a>* pointer variable that receives the interface pointer to the new pointer moniker. When successful, the function has called <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a> on the moniker and the caller is responsible for calling <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a>. When an error occurs, the returned interface pointer has a <b>NULL</b> value.


## -returns



This function can return the standard return values E_OUTOFMEMORY, E_UNEXPECTED, and S_OK.




## -remarks



A pointer moniker wraps an existing interface pointer in a moniker that can be passed to those interfaces that require monikers. Pointer monikers allow an object that has no persistent representation to participate in a moniker-binding operation. 



Pointer monikers are not commonly used, so this function is not often called.





## -see-also




<a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a>
 

 

