---
UID: NF:cscobj.IEnumOfflineFilesSettings.Clone
title: IEnumOfflineFilesSettings::Clone (cscobj.h)
description: Creates a new instance of the enumerator with the same enumeration state as the current one. (IEnumOfflineFilesSettings.Clone)
helpviewer_keywords: ["Clone","Clone method [Offline Files]","Clone method [Offline Files]","IEnumOfflineFilesSettings interface","IEnumOfflineFilesSettings interface [Offline Files]","Clone method","IEnumOfflineFilesSettings.Clone","IEnumOfflineFilesSettings::Clone","cscobj/IEnumOfflineFilesSettings::Clone","of.ienumofflinefilessettings_clone"]
old-location: of\ienumofflinefilessettings_clone.htm
tech.root: of
ms.assetid: 85c2e5a3-4b1c-4a21-8693-804c088a7a56
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Offline Files], Clone method [Offline Files],IEnumOfflineFilesSettings interface, IEnumOfflineFilesSettings interface [Offline Files],Clone method, IEnumOfflineFilesSettings.Clone, IEnumOfflineFilesSettings::Clone, cscobj/IEnumOfflineFilesSettings::Clone, of.ienumofflinefilessettings_clone
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
 - IEnumOfflineFilesSettings::Clone
 - cscobj/IEnumOfflineFilesSettings::Clone
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
 - IEnumOfflineFilesSettings.Clone
---

# IEnumOfflineFilesSettings::Clone


## -description

Creates a new instance of the enumerator with the same enumeration state as the current one.

## -parameters

### -param ppenum [out]

Address of an <a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-ienumofflinefilessettings">IEnumOfflineFilesSettings</a> pointer variable that receives the interface pointer of the new enumeration object.

## -returns

Returns <b>S_OK</b> if the enumerator is created successfully, or an error value otherwise.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-ienumofflinefilessettings">IEnumOfflineFilesSettings</a>
