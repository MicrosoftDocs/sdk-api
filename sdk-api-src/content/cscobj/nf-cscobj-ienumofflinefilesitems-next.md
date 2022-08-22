---
UID: NF:cscobj.IEnumOfflineFilesItems.Next
title: IEnumOfflineFilesItems::Next (cscobj.h)
description: Retrieves the next item in the enumeration and advances the enumerator. (IEnumOfflineFilesItems.Next)
helpviewer_keywords: ["IEnumOfflineFilesItems interface [Offline Files]","Next method","IEnumOfflineFilesItems.Next","IEnumOfflineFilesItems::Next","Next","Next method [Offline Files]","Next method [Offline Files]","IEnumOfflineFilesItems interface","cscobj/IEnumOfflineFilesItems::Next","of.ienumofflinefilesitems_next"]
old-location: of\ienumofflinefilesitems_next.htm
tech.root: of
ms.assetid: 509bb93a-0ab4-4e4a-935a-c30e6b1f03fd
ms.date: 12/05/2018
ms.keywords: IEnumOfflineFilesItems interface [Offline Files],Next method, IEnumOfflineFilesItems.Next, IEnumOfflineFilesItems::Next, Next, Next method [Offline Files], Next method [Offline Files],IEnumOfflineFilesItems interface, cscobj/IEnumOfflineFilesItems::Next, of.ienumofflinefilesitems_next
req.header: cscobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumOfflineFilesItems::Next
 - cscobj/IEnumOfflineFilesItems::Next
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IEnumOfflineFilesItems.Next
---

# IEnumOfflineFilesItems::Next


## -description

Retrieves the next item in the enumeration and advances the enumerator.

## -parameters

### -param celt [in]

Number of elements requested.

### -param rgelt [out]

Array of elements returned.

### -param pceltFetched [out]

Pointer to number of elements actually supplied.

## -returns

Returns <b>S_OK</b> if the number of elements returned is <i>celt</i>; S_FALSE if a number less than <i>celt</i> is returned; or an error value otherwise.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-ienumofflinefilesitems">IEnumOfflineFilesItems</a>
