---
UID: NS:objidl.tagSTGMEDIUM~r1
title: uSTGMEDIUM
ms.date: 01/30/19
ms.keywords: tagSTGMEDIUM, uSTGMEDIUM
ms.topic: language-reference
f1_keywords: ["objidl/tagSTGMEDIUM"]
targetos: Windows
product: Windows
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: objidl.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: uSTGMEDIUM
req.umdf-ver: 
req.unicode-ansi: 
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

Represents a generalized global memory handle used for data transfer operations by the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-iadvisesink">IAdviseSink</a>, <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-iolecache">IOleCache</a> interfaces.


## -struct-fields

### -field tymed

The type of storage medium. The marshaling and unmarshaling routines use this value to determine which union member was used. This value must be one of the elements of the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/ne-objidl-tagtymed">TYMED</a> enumeration.


### -field DUMMYUNIONNAME

### -field hBitmap

Bitmap handle. The tymed member is TYMED_GDI.


### -field hMetaFilePict

Metafile handle. The tymed member is TYMED_MFPICT.


### -field hEnhMetaFile

Enhanced metafile handle. The tymed member is TYMED_ENHMF.


### -field hGlobal

Global memory handle. The tymed member is TYMED_HGLOBAL.


### -field lpszFileName

Pointer to the path of a disk file that contains the data. The tymed member is TYMED_FILE. 


### -field pstm

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface. The tymed member is TYMED_ISTREAM.


### -field pstg

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> interface. The tymed member is TYMED_ISTORAGE.


### -field pUnkForRelease

Pointer to an interface instance that allows the sending process to control the way the storage is released when the receiving process calls the <a href="https://docs.microsoft.com/windows/desktop/api/ole2/nf-ole2-releasestgmedium">ReleaseStgMedium</a> function. If <i>pUnkForRelease</i> is <b>NULL</b>, <b>ReleaseStgMedium</b> uses default procedures to release the storage; otherwise, <b>ReleaseStgMedium</b> uses the specified IUnknown interface.


## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-tagformatetc">FORMATETC</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-iadvisesink">IAdviseSink</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>



<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-iolecache">IOleCache</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ole2/nf-ole2-releasestgmedium">ReleaseStgMedium</a>
 

