---
UID: NF:oleauto.GetRecordInfoFromGuids
title: GetRecordInfoFromGuids function (oleauto.h)
description: Returns a pointer to the IRecordInfo interface for a UDT by passing the GUID of the type information without having to load the type library.
helpviewer_keywords: ["GetRecordInfoFromGuids","GetRecordInfoFromGuids function [Automation]","_oa96_GetRecordInfoFromGuids","automat.getrecordinfofromguids","oleauto/GetRecordInfoFromGuids"]
old-location: automat\getrecordinfofromguids.htm
tech.root: automat
ms.assetid: 0f132a13-ebcd-4886-b842-e6852d6fb2c8
ms.date: 12/05/2018
ms.keywords: GetRecordInfoFromGuids, GetRecordInfoFromGuids function [Automation], _oa96_GetRecordInfoFromGuids, automat.getrecordinfofromguids, oleauto/GetRecordInfoFromGuids
req.header: oleauto.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetRecordInfoFromGuids
 - oleauto/GetRecordInfoFromGuids
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - GetRecordInfoFromGuids
---

# GetRecordInfoFromGuids function


## -description

Returns a pointer to the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-irecordinfo">IRecordInfo</a> interface for a UDT by passing the GUID of the type information without having to load the type library.

## -parameters

### -param rGuidTypeLib [in]

The GUID of the type library containing the UDT.

### -param uVerMajor [in]

The major version number of the type library of the UDT.

### -param uVerMinor [in]

The minor version number of the type library of the UDT.

### -param lcid [in]

The locale ID of the caller.

### -param rGuidTypeInfo [in]

The GUID of the typeinfo that describes the UDT.

### -param ppRecInfo [out]

The <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-irecordinfo">IRecordInfo</a> interface.

## -returns

This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG
</b></dt>
</dl>
</td>
<td width="60%">
One or more of the arguments is not valid.


</td>
</tr>
</table>

## -remarks

A pointer to <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-irecordinfo">IRecordInfo</a> can be serialized by writing out the GUIDs and version numbers and deserialized by loading the information and passing it to <b>GetRecordInfoFromGuids</b>.