---
UID: NF:vsmgmt.IVssEnumMgmtObject.Next
title: IVssEnumMgmtObject::Next (vsmgmt.h)
description: Returns the specified number of objects from the specified list of enumerated objects. (IVssEnumMgmtObject.Next)
helpviewer_keywords: ["IVssEnumMgmtObject interface [VSS]","Next method","IVssEnumMgmtObject.Next","IVssEnumMgmtObject::Next","Next","Next method [VSS]","Next method [VSS]","IVssEnumMgmtObject interface","base.ivssenummgmtobject_next","vsmgmt/IVssEnumMgmtObject::Next"]
old-location: base\ivssenummgmtobject_next.htm
tech.root: base
ms.assetid: 0ddcf25d-dc3e-4522-a98e-98d867230d42
ms.date: 12/05/2018
ms.keywords: IVssEnumMgmtObject interface [VSS],Next method, IVssEnumMgmtObject.Next, IVssEnumMgmtObject::Next, Next, Next method [VSS], Next method [VSS],IVssEnumMgmtObject interface, base.ivssenummgmtobject_next, vsmgmt/IVssEnumMgmtObject::Next
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
 - IVssEnumMgmtObject::Next
 - vsmgmt/IVssEnumMgmtObject::Next
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
 - IVssEnumMgmtObject.Next
---

# IVssEnumMgmtObject::Next


## -description

The <b>Next</b> method 
    returns the specified number of objects from the specified list of enumerated objects.

## -parameters

### -param celt [in]

The number of elements to be read from the list of enumerated objects into the <i>rgelt</i> buffer.

### -param rgelt [out]

The address of a caller-allocated buffer that receives <i>celt</i><a href="/windows/desktop/api/vsmgmt/ns-vsmgmt-vss_mgmt_object_prop">VSS_MGMT_OBJECT_PROP</a> structures that contain the 
      returned objects. This parameter is required and cannot be <b>NULL</b>.

### -param pceltFetched [out]

The number of elements that were returned in the <i>rgelt</i> buffer.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/vsmgmt/nn-vsmgmt-ivssenummgmtobject">IVssEnumMgmtObject</a>



<a href="/windows/desktop/api/vsmgmt/ns-vsmgmt-vss_mgmt_object_prop">VSS_MGMT_OBJECT_PROP</a>
