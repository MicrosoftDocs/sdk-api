---
UID: NS:objidl.tagSTGMEDIUM
title: uSTGMEDIUM (objidl.h)
author: windows-sdk-content
description: Represents a generalized global memory handle used for data transfer operations by the IAdviseSink, IDataObject, and IOleCache interfaces.
old-location: com\stgmedium.htm
tech.root: com
ms.assetid: 5d05819a-10db-4d8e-91e4-8a7c05885cde
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPSTGMEDIUM, ASYNC_STGMEDIUM, LPSTGMEDIUM, LPSTGMEDIUM structure pointer [COM], STGMEDIUM, STGMEDIUM structure [COM], _ole_STGMEDIUM, com.stgmedium, objidl/LPSTGMEDIUM, objidl/STGMEDIUM, uSTGMEDIUM"
ms.topic: struct
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
 - STGMEDIUM
product: Windows
targetos: Windows
req.typenames: uSTGMEDIUM
req.redist: 
---

# uSTGMEDIUM structure


## -description


Represents a generalized global memory handle used for data transfer operations by the <a href="https://msdn.microsoft.com/bc9f217a-75bd-4155-9d00-df44b00cf0e5">IAdviseSink</a>, <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>, and <a href="https://msdn.microsoft.com/b5ef85d0-b54e-4831-87f1-ac6763179181">IOleCache</a> interfaces.


## -struct-fields




### -field tymed

The ype of storage medium. The marshaling and unmarshaling routines use this value to determine which union member was used. This value must be one of the elements of the <a href="https://msdn.microsoft.com/ac41286f-7c67-444a-81b7-21b61079bbf5">TYMED</a> enumeration.


### -field u

Handle, string, or interface pointer that the receiving process can use to access the data being transferred. If tymed is TYMED_NULL, the union member is undefined; otherwise, it is one of the following values.



##### hBitmap

Bitmap handle. The tymed member is TYMED_GDI.



##### hMetaFilePict

 Metafile handle. The tymed member is TYMED_MFPICT.



##### hEnhMetaFile

Enhanced metafile handle. The tymed member is TYMED_ENHMF.



##### hGlobal

Global memory handle. The tymed member is TYMED_HGLOBAL.



##### lpszFileName

 Pointer to the path of a disk file that contains the data. The tymed member is TYMED_FILE. 




##### pstm

Pointer to an <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> interface. The tymed member is TYMED_ISTREAM.



##### pstg

Pointer to an <a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> interface. The tymed member is TYMED_ISTORAGE.


### -field u.hBitmap

 


### -field u.hMetaFilePict

 


### -field u.hEnhMetaFile

 


### -field u.hGlobal

 


### -field u.lpszFileName

 


### -field u.pstm

 


### -field u.pstg

 


### -field pUnkForRelease

Pointer to an interface instance that allows the sending process to control the way the storage is released when the receiving process calls the <a href="https://msdn.microsoft.com/da7d7bcb-0b5b-4053-8f0e-ff311c424375">ReleaseStgMedium</a> function. If <i>pUnkForRelease</i> is <b>NULL</b>, <b>ReleaseStgMedium</b> uses default procedures to release the storage; otherwise, <b>ReleaseStgMedium</b> uses the specified IUnknown interface.



## -see-also




<a href="https://msdn.microsoft.com/4478eb9a-84a1-4f3a-8290-94b8dd20c081">FORMATETC</a>



<a href="https://msdn.microsoft.com/bc9f217a-75bd-4155-9d00-df44b00cf0e5">IAdviseSink</a>



<a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>



<a href="https://msdn.microsoft.com/b5ef85d0-b54e-4831-87f1-ac6763179181">IOleCache</a>



<a href="https://msdn.microsoft.com/da7d7bcb-0b5b-4053-8f0e-ff311c424375">ReleaseStgMedium</a>
 

 

