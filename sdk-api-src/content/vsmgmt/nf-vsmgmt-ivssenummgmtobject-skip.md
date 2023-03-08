---
UID: NF:vsmgmt.IVssEnumMgmtObject.Skip
title: IVssEnumMgmtObject::Skip (vsmgmt.h)
description: Skips the specified number of objects. (IVssEnumMgmtObject.Skip)
helpviewer_keywords: ["IVssEnumMgmtObject interface [VSS]","Skip method","IVssEnumMgmtObject.Skip","IVssEnumMgmtObject::Skip","Skip","Skip method [VSS]","Skip method [VSS]","IVssEnumMgmtObject interface","base.ivssenummgmtobject_skip","vsmgmt/IVssEnumMgmtObject::Skip"]
old-location: base\ivssenummgmtobject_skip.htm
tech.root: base
ms.assetid: ec53ac62-deb3-46f3-947a-1f6a4add4db2
ms.date: 12/05/2018
ms.keywords: IVssEnumMgmtObject interface [VSS],Skip method, IVssEnumMgmtObject.Skip, IVssEnumMgmtObject::Skip, Skip, Skip method [VSS], Skip method [VSS],IVssEnumMgmtObject interface, base.ivssenummgmtobject_skip, vsmgmt/IVssEnumMgmtObject::Skip
req.header: vsmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssEnumMgmtObject::Skip
 - vsmgmt/IVssEnumMgmtObject::Skip
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VsMgmt.h
api_name:
 - IVssEnumMgmtObject.Skip
---

# IVssEnumMgmtObject::Skip


## -description

The <b>Skip</b> method skips the specified 
    number of objects.

## -parameters

### -param celt [in]

Number of elements to be skipped in the list of enumerated objects.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/vsmgmt/nn-vsmgmt-ivssenummgmtobject">IVssEnumMgmtObject</a>
