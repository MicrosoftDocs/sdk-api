---
UID: NF:wabiab.IAddrBook.GetSearchPath
tech.root: wab wab 
title: IAddrBook::GetSearchPath
ms.date: 08/03/2022
ms.topic: language-reference
targetos: Windows
description: IAddrBook::GetSearchPath returns an ordered list of the entry identifiers of containers to be included in the name resolution process initiated by the IAddrBook::ResolveName method.
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: wabiab.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - wabiab.h
api_name:
 - IAddrBook::GetSearchPath
f1_keywords:
 - IAddrBook::GetSearchPath
 - wabiab/IAddrBook::GetSearchPath
dev_langs:
 - c++
---

## -description

Returns an ordered list of the entry identifiers of containers to be included in the name resolution process initiated by the [IAddrBook::ResolveName](nf-wabiab-iaddrbook-resolvename.md) method.

## -parameters

### -param ulFlags

Value of type **ULONG** that specifies the bitmask of flags that control the type of the strings returned in the search path. The following flag is valid for the Windows Address Book (WAB):

| Flag | Description |
|------|-------------|
| MAPI_UNICODE | Specifies that returned strings are formatted in Unicode. If this flag is not set, the strings will be in ANSI format. |

### -param lppSearchPath

Address of a pointer to a variable of type **SRowSet** that specifies the ordered list of container entry identifiers. **IAddrBook::GetSearchPath** stores the ordered list in an **SRowSet** structure. If there are no containers in the address book hierarchy, the method returns zero in the **SRowSet** structure.

## -returns

HRESULT

## -remarks

## -see-also

