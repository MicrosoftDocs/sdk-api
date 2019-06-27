---
UID: NE:objidl.tagTYMED
title: TYMED (objidl.h)
author: windows-sdk-content
description: Indicates the type of storage medium being used in a data transfer. They are used in the STGMEDIUM or FORMATETC structures.
old-location: com\tymed.htm
tech.root: com
ms.assetid: ac41286f-7c67-444a-81b7-21b61079bbf5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: TYMED, TYMED enumeration [COM], TYMED_ENHMF, TYMED_FILE, TYMED_GDI, TYMED_HGLOBAL, TYMED_ISTORAGE, TYMED_ISTREAM, TYMED_MFPICT, TYMED_NULL, _ole_TYMED, com.tymed, objidl/TYMED, objidl/TYMED_ENHMF, objidl/TYMED_FILE, objidl/TYMED_GDI, objidl/TYMED_HGLOBAL, objidl/TYMED_ISTORAGE, objidl/TYMED_ISTREAM, objidl/TYMED_MFPICT, objidl/TYMED_NULL
ms.topic: enum
f1_keywords: 
 - "objidl/TYMED"
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ObjIdl.h
api_name:
 - TYMED
product: Windows
targetos: Windows
req.typenames: TYMED
req.redist: 
ms.custom: 19H1
---

# TYMED enumeration


## -description


Indicates the type of storage medium being used in a data transfer. They are used in the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-tagstgmedium">STGMEDIUM</a> or <a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-tagformatetc">FORMATETC</a> structures.


## -enum-fields




### -field TYMED_HGLOBAL

The storage medium is a global memory handle (<b>HGLOBAL</b>). Allocate the global handle with the GMEM_MOVEABLE flag. If the <b>punkForRelease</b> member of <a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-tagstgmedium">STGMEDIUM</a> is <b>NULL</b>, the destination process should use <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-globalfree">GlobalFree</a> to release the memory.


### -field TYMED_FILE

The storage medium is a disk file identified by a path. If the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-tagstgmedium">STGMEDIUM</a> <b>punkForRelease</b> member is <b>NULL</b>, the destination process should use <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-openfile">OpenFile</a> to delete the file.


### -field TYMED_ISTREAM

The storage medium is a stream object identified by an <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> pointer. Use <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-isequentialstream-read">ISequentialStream::Read</a> to read the data. If the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-tagstgmedium">STGMEDIUM</a> <b>punkForRelease</b> member is not <b>NULL</b>, the destination process should use <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> to release the stream component.


### -field TYMED_ISTORAGE

The storage medium is a storage component identified by an <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> pointer. The data is in the streams and storages contained by this <b>IStorage</b> instance. If the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-tagstgmedium">STGMEDIUM</a> <b>punkForRelease</b> member is not <b>NULL</b>, the destination process should use <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> to release the storage component.


### -field TYMED_GDI

The storage medium is a GDI component (<b>HBITMAP</b>). If the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-tagstgmedium">STGMEDIUM</a> <b>punkForRelease</b> member is <b>NULL</b>, the destination process should use <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a> to delete the bitmap.


### -field TYMED_MFPICT

The storage medium is a metafile (<b>HMETAFILE</b>). Use the GDI functions to access the metafile's data. If the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-tagstgmedium">STGMEDIUM</a> <b>punkForRelease</b> member is <b>NULL</b>, the destination process should use <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-deletemetafile">DeleteMetaFile</a> to delete the bitmap.


### -field TYMED_ENHMF

The storage medium is an enhanced metafile. If the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-tagstgmedium">STGMEDIUM</a> <b>punkForRelease</b> member is <b>NULL</b>, the destination process should use <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-deleteenhmetafile">DeleteEnhMetaFile</a> to delete the bitmap.


### -field TYMED_NULL

No data is being passed.



## -remarks



During data transfer operations, a storage medium is specified. This medium must be released after the data transfer operation. The provider of the medium indicates its choice of ownership scenarios in the value it provides in the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-tagstgmedium">STGMEDIUM</a> structure. A <b>NULL</b> value for the <b>pUnkForRelease</b> member indicates that the receiving body of code owns and can free the medium. A non-<b>NULL</b> pointer specifies that <a href="https://docs.microsoft.com/windows/desktop/api/ole2/nf-ole2-releasestgmedium">ReleaseStgMedium</a> can always be called to free the medium.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-tagformatetc">FORMATETC</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-iadvisesink">IAdviseSink</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>



<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-iolecache">IOleCache</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ole2/nf-ole2-releasestgmedium">ReleaseStgMedium</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-tagstgmedium">STGMEDIUM</a>
 

 

