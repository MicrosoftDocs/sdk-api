---
UID: NF:shobjidl_core.IEnumIDList.Next
title: IEnumIDList::Next (shobjidl_core.h)
description: Retrieves the specified number of item identifiers in the enumeration sequence and advances the current position by the number of items retrieved.
helpviewer_keywords: ["IEnumIDList interface [Windows Shell]","Next method","IEnumIDList.Next","IEnumIDList::Next","Next","Next method [Windows Shell]","Next method [Windows Shell]","IEnumIDList interface","_win32_IEnumIDList_Next","shell.IEnumIDList_Next","shobjidl_core/IEnumIDList::Next"]
old-location: shell\IEnumIDList_Next.htm
tech.root: shell
ms.assetid: 4b2cd7a3-687c-4a51-b9af-a01576463f0b
ms.date: 12/05/2018
ms.keywords: IEnumIDList interface [Windows Shell],Next method, IEnumIDList.Next, IEnumIDList::Next, Next, Next method [Windows Shell], Next method [Windows Shell],IEnumIDList interface, _win32_IEnumIDList_Next, shell.IEnumIDList_Next, shobjidl_core/IEnumIDList::Next
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumIDList::Next
 - shobjidl_core/IEnumIDList::Next
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IEnumIDList.Next
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

The address of a pointer to an array of <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> pointers that receive the item identifiers. The implementation must allocate these item identifiers using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a>. The calling application is responsible for freeing the item identifiers using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.
					
                    

The <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structures returned in the array are relative to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> being enumerated.

### -param pceltFetched [out]

Type: <b>ULONG*</b>

A pointer to a value that receives a count of the item identifiers actually returned in <i>rgelt</i>. The count can be smaller than the value specified in the <i>celt</i> parameter. This parameter can be <b>NULL</b> on entry only if <i>celt</i> = 1, because in that case the method can only retrieve one (S_OK) or zero (S_FALSE) items.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if the method successfully retrieved the requested <i>celt</i> elements. This method only returns S_OK if the full count of requested items are successfully retrieved.
                    
                    

S_FALSE indicates that more items were requested than remained in the enumeration. The value pointed to by the <i>pceltFetched</i> parameter specifies the actual number of items retrieved. Note that the value will be 0 if there are no more items to retrieve.

Returns a COM-defined error value otherwise.

## -remarks

If this method returns a Component Object Model (COM) error code (as determined by the <a href="/windows/desktop/api/winerror/nf-winerror-failed">FAILED</a> macro), then no entries in the <i>rgelt</i> array are valid on exit. If this method returns a success code (such as S_OK or S_FALSE), then the <b>ULONG</b> pointed to by the <i>pceltFetched</i> parameter determines how many entries in the <i>rgelt</i> array are valid on exit.

The distinction is important in the case where <i>celt</i> &gt; 1. For example, if you pass <i>celt</i>=10 and there are only 3 elements left, *<i>pceltFetched</i> will be 3 and the method will return S_FALSE meaning that you reached the end of the file. The three fetched elements will be stored into <i>rgelt</i> and are valid.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist">IEnumIDList</a>