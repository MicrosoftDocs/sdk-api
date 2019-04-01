---
UID: NS:objidl.tagSTGMEDIUM~r1
title: uSTGMEDIUM
ms.date: 01/30/19
ms.keywords: tagSTGMEDIUM, uSTGMEDIUM
ms.topic: language-reference
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

Represents a generalized global memory handle used for data transfer operations by the <a href="https://msdn.microsoft.com/bc9f217a-75bd-4155-9d00-df44b00cf0e5">IAdviseSink</a>, <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>, and <a href="https://msdn.microsoft.com/b5ef85d0-b54e-4831-87f1-ac6763179181">IOleCache</a> interfaces.


## -struct-fields

### -field tymed

The type of storage medium. The marshaling and unmarshaling routines use this value to determine which union member was used. This value must be one of the elements of the <a href="https://msdn.microsoft.com/ac41286f-7c67-444a-81b7-21b61079bbf5">TYMED</a> enumeration.


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

Pointer to an <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> interface. The tymed member is TYMED_ISTREAM.


### -field pstg

Pointer to an <a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> interface. The tymed member is TYMED_ISTORAGE.


### -field pUnkForRelease

Pointer to an interface instance that allows the sending process to control the way the storage is released when the receiving process calls the <a href="https://msdn.microsoft.com/da7d7bcb-0b5b-4053-8f0e-ff311c424375">ReleaseStgMedium</a> function. If <i>pUnkForRelease</i> is <b>NULL</b>, <b>ReleaseStgMedium</b> uses default procedures to release the storage; otherwise, <b>ReleaseStgMedium</b> uses the specified IUnknown interface.


## -see-also

<a href="https://msdn.microsoft.com/4478eb9a-84a1-4f3a-8290-94b8dd20c081">FORMATETC</a>



<a href="https://msdn.microsoft.com/bc9f217a-75bd-4155-9d00-df44b00cf0e5">IAdviseSink</a>



<a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>



<a href="https://msdn.microsoft.com/b5ef85d0-b54e-4831-87f1-ac6763179181">IOleCache</a>



<a href="https://msdn.microsoft.com/da7d7bcb-0b5b-4053-8f0e-ff311c424375">ReleaseStgMedium</a>
 

