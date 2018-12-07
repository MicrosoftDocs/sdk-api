---
UID: NF:shobjidl_core.IEnumIDList.Next
title: IEnumIDList::Next
author: windows-sdk-content
description: Retrieves the specified number of item identifiers in the enumeration sequence and advances the current position by the number of items retrieved.
old-location: shell\IEnumIDList_Next.htm
tech.root: shell
ms.assetid: 4b2cd7a3-687c-4a51-b9af-a01576463f0b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IEnumIDList interface [Windows Shell],Next method, IEnumIDList.Next, IEnumIDList::Next, Next, Next method [Windows Shell], Next method [Windows Shell],IEnumIDList interface, _win32_IEnumIDList_Next, shell.IEnumIDList_Next, shobjidl_core/IEnumIDList::Next
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
 - IEnumIDList.Next
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumIDList::Next


## -description


Retrieves the specified number of item identifiers in the enumeration sequence and advances the current position by the number of items retrieved.


## -parameters




### -param celt [in]

Type: <b>ULONG</b>

The number of elements in the array referenced by the <i>rgelt</i> parameter.


### -param rgelt [out]

Type: <b>LPITEMIDLIST*</b>

The address of a pointer to an array of <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> pointers that receive the item identifiers. The implementation must allocate these item identifiers using <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a>. The calling application is responsible for freeing the item identifiers using <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.
					
                    

The <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structures returned in the array are relative to the <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a> being enumerated.


### -param pceltFetched [out]

Type: <b>ULONG*</b>

A pointer to a value that receives a count of the item identifiers actually returned in <i>rgelt</i>. The count can be smaller than the value specified in the <i>celt</i> parameter. This parameter can be <b>NULL</b> on entry only if <i>celt</i> = 1, because in that case the method can only retrieve one (S_OK) or zero (S_FALSE) items.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if the method successfully retrieved the requested <i>celt</i> elements. This method only returns S_OK if the full count of requested items are successfully retrieved.
                    
                    

S_FALSE indicates that more items were requested than remained in the enumeration. The value pointed to by the <i>pceltFetched</i> parameter specifies the actual number of items retrieved. Note that the value will be 0 if there are no more items to retrieve.

Returns a COM-defined error value otherwise.




## -remarks



If this method returns a Component Object Model (COM) error code (as determined by the <a href="https://msdn.microsoft.com/d9c4ff73-c255-4a82-b901-23bd5b41ee6c">FAILED</a> macro), then no entries in the <i>rgelt</i> array are valid on exit. If this method returns a success code (such as S_OK or S_FALSE), then the <b>ULONG</b> pointed to by the <i>pceltFetched</i> parameter determines how many entries in the <i>rgelt</i> array are valid on exit.

The distinction is important in the case where <i>celt</i> &gt; 1. For example, if you pass <i>celt</i>=10 and there are only 3 elements left, *<i>pceltFetched</i> will be 3 and the method will return S_FALSE meaning that you reached the end of the file. The three fetched elements will be stored into <i>rgelt</i> and are valid.
      




## -see-also




<a href="https://msdn.microsoft.com/b6f139d3-c54c-4350-9d8b-cd534909a488">IEnumIDList</a>
 

 

