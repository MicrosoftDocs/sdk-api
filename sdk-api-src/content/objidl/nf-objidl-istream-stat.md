---
UID: NF:objidl.IStream.Stat
title: IStream::Stat (objidl.h)
description: The Stat method retrieves the STATSTG structure for this stream.
helpviewer_keywords: ["IStream interface [Structured Storage]","Stat method","IStream.Stat","IStream::Stat","Stat","Stat method [Structured Storage]","Stat method [Structured Storage]","IStream interface","_stg_istream_stat","objidl/IStream::Stat","stg.istream_stat"]
old-location: stg\istream_stat.htm
tech.root: Stg
ms.assetid: c22ab396-dbc5-43a0-8448-35a2c094464f
ms.date: 12/05/2018
ms.keywords: IStream interface [Structured Storage],Stat method, IStream.Stat, IStream::Stat, Stat, Stat method [Structured Storage], Stat method [Structured Storage],IStream interface, _stg_istream_stat, objidl/IStream::Stat, stg.istream_stat
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IStream::Stat
 - objidl/IStream::Stat
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ole32.dll
api_name:
 - IStream.Stat
---

# IStream::Stat


## -description

The <b>Stat</b> method retrieves the 
<a href="/windows/desktop/api/objidl/ns-objidl-statstg">STATSTG</a> structure for this stream.

## -parameters

### -param pstatstg [out]

Pointer to a 
<a href="/windows/desktop/api/objidl/ns-objidl-statstg">STATSTG</a> structure where this method places information about this stream object.

### -param grfStatFlag [in]

Specifies that this method does not return some of the members in the 
<a href="/windows/desktop/api/objidl/ns-objidl-statstg">STATSTG</a> structure, thus saving a memory allocation operation. Values are taken from the 
<a href="/windows/desktop/api/wtypes/ne-wtypes-statflag">STATFLAG</a> enumeration.

## -returns

This method can return one of these values.

| Return code | Description |
|----------------|---------------|
|S_OK | The STATSTG structure was successfully returned at the specified location.|
|E_PENDING | Asynchronous Storage only: Part or all of the stream's data is currently unavailable. |
|STG_E_ACCESSDENIED | The caller does not have enough permissions for accessing statistics for this storage object.|
|STG_E_INSUFFICIENTMEMORY | The STATSTG structure was not returned due to a lack of memory.|
|STG_E_INVALIDFLAG | The value for the *grfStateFlag* parameter is not valid.|
|STG_E_INVALIDPOINTER | The *pStatStg* pointer is not valid.|
|STG_E_REVERTED | The object has been invalidated by a revert operation above it in the transaction tree.|

## -remarks

<b>IStream::Stat</b> retrieves a pointer to the 
<a href="/windows/desktop/api/objidl/ns-objidl-statstg">STATSTG</a> structure that contains information about this open stream. When this stream is within a structured storage and 
<a href="/windows/desktop/api/objidl/nf-objidl-istorage-enumelements">IStorage::EnumElements</a> is called, it creates an enumerator object with the 
<a href="/windows/desktop/api/objidl/nn-objidl-ienumstatstg">IEnumSTATSTG</a> interface on it, which can be called to enumerate the storages and streams through the 
<b>STATSTG</b> structures associated with each of them.

## -see-also

<a href="/windows/desktop/Stg/istream-compound-file-implementation">IStream - Compound File Implementation</a>



<a href="/windows/desktop/api/wtypes/ne-wtypes-statflag">STATFLAG</a>



<a href="/windows/desktop/api/objidl/ns-objidl-statstg">STATSTG</a>