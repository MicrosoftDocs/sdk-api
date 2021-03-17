---
UID: NF:shobjidl_core.IEnumFullIDList.Next
title: IEnumFullIDList::Next (shobjidl_core.h)
description: Retrieves a specified number of IDLIST_ABSOLUTE items.
helpviewer_keywords: ["IEnumFullIDList interface [Windows Shell]","Next method","IEnumFullIDList.Next","IEnumFullIDList::Next","Next","Next method [Windows Shell]","Next method [Windows Shell]","IEnumFullIDList interface","_shell_IEnumFullIDList_Next","shell.IEnumFullIDList_Next","shobjidl_core/IEnumFullIDList::Next"]
old-location: shell\IEnumFullIDList_Next.htm
tech.root: shell
ms.assetid: 023f8935-0382-404e-b1bf-737824cf0f34
ms.date: 12/05/2018
ms.keywords: IEnumFullIDList interface [Windows Shell],Next method, IEnumFullIDList.Next, IEnumFullIDList::Next, Next, Next method [Windows Shell], Next method [Windows Shell],IEnumFullIDList interface, _shell_IEnumFullIDList_Next, shell.IEnumFullIDList_Next, shobjidl_core/IEnumFullIDList::Next
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumFullIDList::Next
 - shobjidl_core/IEnumFullIDList::Next
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IEnumFullIDList.Next
---

# IEnumFullIDList::Next


## -description

Retrieves a specified number of IDLIST_ABSOLUTE items.

## -parameters

### -param celt [in]

Type: <b>ULONG</b>

The number of items referenced in the array referenced by the <i>rgelt</i> parameter.

### -param rgelt [out]

Type: <b>PIDLIST_ABSOLUTE*</b>

On success, contains a PIDL array. The implementation must allocate these item identifiers using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a>. The calling application is responsible for freeing the item identifiers using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

### -param pceltFetched [out]

Type: <b>ULONG*</b>

On success, contains a pointer to a value that receives a count of the absolute item identifiers actually returned in <i>rgelt</i>. The count can be smaller than the value specified in the <i>celt</i> parameter. This parameter can be <b>NULL</b> on entry only if <i>celt</i> is 1, because in that case the method can only retrieve one (S_OK) or zero (S_FALSE) items.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if the method successfully retrieved the requested <i>celt</i> elements. This method only returns S_OK if the full count of requested items are successfully retrieved.
                    
                    

S_FALSE indicates that more items were requested than remained in the enumeration. The value pointed to by the <i>pceltFetched</i> parameter specifies the actual number of items retrieved. Note that the value will be 0 if there are no more items to retrieve.

Returns a COM-defined error value otherwise.