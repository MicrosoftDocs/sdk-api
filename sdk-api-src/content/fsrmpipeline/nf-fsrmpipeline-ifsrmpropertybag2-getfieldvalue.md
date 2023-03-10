---
UID: NF:fsrmpipeline.IFsrmPropertyBag2.GetFieldValue
title: IFsrmPropertyBag2::GetFieldValue (fsrmpipeline.h)
description: Gets the value of the specified field from the property bag.
helpviewer_keywords: ["GetFieldValue","GetFieldValue method [File Server Resource Manager]","GetFieldValue method [File Server Resource Manager]","IFsrmPropertyBag2 interface","IFsrmPropertyBag2 interface [File Server Resource Manager]","GetFieldValue method","IFsrmPropertyBag2.GetFieldValue","IFsrmPropertyBag2::GetFieldValue","fs.ifsrmpropertybag2_getfieldvalue","fsrm.ifsrmpropertybag2_getfieldvalue","fsrmpipeline/IFsrmPropertyBag2::GetFieldValue"]
old-location: fsrm\ifsrmpropertybag2_getfieldvalue.htm
tech.root: fsrm
ms.assetid: ccd52bbc-998e-435f-bea5-ed456adf3ff9
ms.date: 12/05/2018
ms.keywords: GetFieldValue, GetFieldValue method [File Server Resource Manager], GetFieldValue method [File Server Resource Manager],IFsrmPropertyBag2 interface, IFsrmPropertyBag2 interface [File Server Resource Manager],GetFieldValue method, IFsrmPropertyBag2.GetFieldValue, IFsrmPropertyBag2::GetFieldValue, fs.ifsrmpropertybag2_getfieldvalue, fsrm.ifsrmpropertybag2_getfieldvalue, fsrmpipeline/IFsrmPropertyBag2::GetFieldValue
req.header: fsrmpipeline.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FsrmPipeline.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFsrmPropertyBag2::GetFieldValue
 - fsrmpipeline/IFsrmPropertyBag2::GetFieldValue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmPropertyBag2.GetFieldValue
---

# IFsrmPropertyBag2::GetFieldValue


## -description

Gets the value of the specified field from the property bag.

## -parameters

### -param field [in]

Type: <b><a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmpropertybagfield">FsrmPropertyBagField</a></b>

Indicates whether the volume name returned is the name of the volume being accessed, which may be a snapshot, or the volume where the property bag lives.

### -param value [out, retval]

Type: <b>VARIANT*</b>

Returns the specified value.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmpropertybagfield">FsrmPropertyBagField</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmpropertybag2">IFsrmPropertyBag2</a>