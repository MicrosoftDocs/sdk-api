---
UID: NS:objidl.tagSTGMEDIUM~r1
title: uSTGMEDIUM
description: The uSTGMEDIUM structure represents a generalized global memory handle used for data transfer operations by the IAdviseSink, IDataObject, and IOleCache interfaces.
ms.date: 08/13/2022
ms.keywords: tagSTGMEDIUM, uSTGMEDIUM
targetos: Windows
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: objidl.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.typenames: uSTGMEDIUM
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - tagSTGMEDIUM
 - objidl/tagSTGMEDIUM
 - uSTGMEDIUM
 - objidl/uSTGMEDIUM
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - objidl.h
api_name:
 - tagSTGMEDIUM
 - uSTGMEDIUM
---

# uSTGMEDIUM structure


## -description

Represents a generalized global memory handle used for data transfer operations by the <a href="/windows/desktop/api/objidl/nn-objidl-iadvisesink">IAdviseSink</a>, <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>, and <a href="/windows/desktop/api/oleidl/nn-oleidl-iolecache">IOleCache</a> interfaces.

## -struct-fields

### -field tymed

The type of storage medium. The marshaling and unmarshaling routines use this value to determine which union member was used. This value must be one of the elements of the <a href="/windows/desktop/api/objidl/ne-objidl-tymed">TYMED</a> enumeration.

### -field DUMMYUNIONNAME

Handle, string, or interface pointer that the receiving process can use to access the data being transferred. If tymed is TYMED_NULL, the union member is undefined; otherwise, it is one of the following values.

### -field DUMMYUNIONNAME.hBitmap

Bitmap handle. The tymed member is TYMED_GDI.

### -field DUMMYUNIONNAME.hMetaFilePict

Metafile handle. The tymed member is TYMED_MFPICT.

### -field DUMMYUNIONNAME.hEnhMetaFile

Enhanced metafile handle. The tymed member is TYMED_ENHMF.

### -field DUMMYUNIONNAME.hGlobal

Global memory handle. The tymed member is TYMED_HGLOBAL.

### -field DUMMYUNIONNAME.lpszFileName

Pointer to the path of a disk file that contains the data. The tymed member is TYMED_FILE.

### -field DUMMYUNIONNAME.pstm

Pointer to an <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface. The tymed member is TYMED_ISTREAM.

### -field DUMMYUNIONNAME.pstg

Pointer to an <a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> interface. The tymed member is TYMED_ISTORAGE.

### -field pUnkForRelease

Pointer to an interface instance that allows the sending process to control the way the storage is released when the receiving process calls the <a href="/windows/desktop/api/ole2/nf-ole2-releasestgmedium">ReleaseStgMedium</a> function. If <i>pUnkForRelease</i> is <b>NULL</b>, <b>ReleaseStgMedium</b> uses default procedures to release the storage; otherwise, <b>ReleaseStgMedium</b> uses the specified IUnknown interface.

## -see-also

<a href="/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a>



<a href="/windows/desktop/api/objidl/nn-objidl-iadvisesink">IAdviseSink</a>



<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-iolecache">IOleCache</a>



<a href="/windows/desktop/api/ole2/nf-ole2-releasestgmedium">ReleaseStgMedium</a>
