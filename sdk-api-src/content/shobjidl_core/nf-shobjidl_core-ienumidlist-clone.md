---
UID: NF:shobjidl_core.IEnumIDList.Clone
title: IEnumIDList::Clone
author: windows-sdk-content
description: Creates a new item enumeration object with the same contents and state as the current one.
old-location: shell\IEnumIDList_Clone.htm
tech.root: shell
ms.assetid: f0118153-25ea-42d6-90bf-b85ffd99b74b
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: Clone, Clone method [Windows Shell], Clone method [Windows Shell],IEnumIDList interface, IEnumIDList interface [Windows Shell],Clone method, IEnumIDList.Clone, IEnumIDList::Clone, _win32_IEnumIDList_Clone, shell.IEnumIDList_Clone, shobjidl_core/IEnumIDList::Clone
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IEnumIDList.Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumIDList::Clone


## -description


Creates a new item enumeration object with the same contents and state as the current one.


## -parameters




### -param ppenum

Type: <b><a href="https://msdn.microsoft.com/b6f139d3-c54c-4350-9d8b-cd534909a488">IEnumIDList</a>**</b>

The address of a pointer to the new enumeration object. The calling application must eventually free the new object by calling its <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> member function.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM-defined error value otherwise.




## -remarks



This method makes it possible to record a particular point in the enumeration sequence and then return to that point at a later time.




## -see-also




<a href="https://msdn.microsoft.com/b6f139d3-c54c-4350-9d8b-cd534909a488">IEnumIDList</a>
 

 

