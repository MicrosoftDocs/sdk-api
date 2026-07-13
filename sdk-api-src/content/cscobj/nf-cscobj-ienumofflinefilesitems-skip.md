---
UID: NF:cscobj.IEnumOfflineFilesItems.Skip
title: IEnumOfflineFilesItems::Skip (cscobj.h)
description: Skips over the next specified number of elements in the enumeration. (IEnumOfflineFilesItems.Skip)
helpviewer_keywords: ["IEnumOfflineFilesItems interface [Offline Files]","Skip method","IEnumOfflineFilesItems.Skip","IEnumOfflineFilesItems::Skip","Skip","Skip method [Offline Files]","Skip method [Offline Files]","IEnumOfflineFilesItems interface","cscobj/IEnumOfflineFilesItems::Skip","of.ienumofflinefilesitems_skip"]
old-location: of\ienumofflinefilesitems_skip.htm
tech.root: of
ms.assetid: e1f201c4-6ca8-49ca-af05-003a09ec86bd
ms.date: 12/05/2018
ms.keywords: IEnumOfflineFilesItems interface [Offline Files],Skip method, IEnumOfflineFilesItems.Skip, IEnumOfflineFilesItems::Skip, Skip, Skip method [Offline Files], Skip method [Offline Files],IEnumOfflineFilesItems interface, cscobj/IEnumOfflineFilesItems::Skip, of.ienumofflinefilesitems_skip
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
 - IEnumOfflineFilesItems::Skip
 - cscobj/IEnumOfflineFilesItems::Skip
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
 - IEnumOfflineFilesItems.Skip
---

# IEnumOfflineFilesItems::Skip


## -description

Skips over the next specified number of elements in the enumeration.

## -parameters

### -param celt [in]

Number of elements to be skipped.

## -returns

Returns <b>S_OK</b> if the number of elements skipped is <i>celt</i>; S_FALSE if a number less than <i>celt</i> is skipped; or an error value otherwise.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-ienumofflinefilesitems">IEnumOfflineFilesItems</a>
