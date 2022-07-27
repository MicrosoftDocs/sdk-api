---
UID: NF:cscobj.IEnumOfflineFilesSettings.Next
title: IEnumOfflineFilesSettings::Next (cscobj.h)
description: Retrieves the next item in the enumeration and advances the enumerator. (IEnumOfflineFilesSettings.Next)
helpviewer_keywords: ["IEnumOfflineFilesSettings interface [Offline Files]","Next method","IEnumOfflineFilesSettings.Next","IEnumOfflineFilesSettings::Next","Next","Next method [Offline Files]","Next method [Offline Files]","IEnumOfflineFilesSettings interface","cscobj/IEnumOfflineFilesSettings::Next","of.ienumofflinefilessettings_next"]
old-location: of\ienumofflinefilessettings_next.htm
tech.root: of
ms.assetid: 00230021-6069-4e0b-a3d6-95651aa6e44a
ms.date: 12/05/2018
ms.keywords: IEnumOfflineFilesSettings interface [Offline Files],Next method, IEnumOfflineFilesSettings.Next, IEnumOfflineFilesSettings::Next, Next, Next method [Offline Files], Next method [Offline Files],IEnumOfflineFilesSettings interface, cscobj/IEnumOfflineFilesSettings::Next, of.ienumofflinefilessettings_next
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
 - IEnumOfflineFilesSettings::Next
 - cscobj/IEnumOfflineFilesSettings::Next
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
 - IEnumOfflineFilesSettings.Next
---

# IEnumOfflineFilesSettings::Next


## -description

Retrieves the next item in the enumeration and advances the enumerator.

## -parameters

### -param celt [in]

Number of elements requested.

### -param rgelt [out]

Array of elements returned.

### -param pceltFetched [out]

Number of elements returned.

## -returns

Returns <b>S_OK</b> if the number of elements returned is <i>celt</i>; S_FALSE if a number less than <i>celt</i> is returned; or an error value otherwise.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-ienumofflinefilessettings">IEnumOfflineFilesSettings</a>
