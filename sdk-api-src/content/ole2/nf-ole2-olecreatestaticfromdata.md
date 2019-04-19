---
UID: NF:ole2.OleCreateStaticFromData
title: OleCreateStaticFromData function (ole2.h)
author: windows-sdk-content
description: Creates a static object, that contains only a representation, with no native data, from a data transfer object.
old-location: com\olecreatestaticfromdata.htm
tech.root: com
ms.assetid: 847d82f5-149d-48a4-a228-f5551a07a790
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: OleCreateStaticFromData, OleCreateStaticFromData function [COM], _ole_OleCreateStaticFromData, com.olecreatestaticfromdata, ole2/OleCreateStaticFromData
ms.topic: function
req.header: ole2.h
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
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
api_name:
 - OleCreateStaticFromData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# OleCreateStaticFromData function


## -description


Creates a static object, that contains only a representation, with no native data, from a data transfer object.


<div class="alert"><b>Note</b>  The OLESTREAM to <a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> conversion functions also convert static objects.</div><div> </div>

## -parameters




### -param pSrcDataObj [in]

Pointer to the <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> interface on the data transfer object that holds the data from which the object will be created.


### -param iid [in]

Reference to the identifier of the interface with which the caller is to communicate with the new object (usually IID_IOleObject, defined in the OLE headers as the interface identifier for <a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a>).


### -param renderopt [in]

Value from the enumeration <a href="https://msdn.microsoft.com/bab871ba-4ec4-49fd-854a-585732b91290">OLERENDER</a> indicating the locally cached drawing or data-retrieval capabilities that the container wants in the newly created component. It is an error to pass the render options OLERENDER_NONE or OLERENDER_ASIS to this function.


### -param pFormatEtc [in]

Depending on which of the <a href="https://msdn.microsoft.com/bab871ba-4ec4-49fd-854a-585732b91290">OLERENDER</a> flags is used as the value of <i>renderopt</i>, may be a pointer to one of the <a href="https://msdn.microsoft.com/4478eb9a-84a1-4f3a-8290-94b8dd20c081">FORMATETC</a> enumeration values. Refer to the <b>OLERENDER</b> enumeration for restrictions.


### -param pClientSite [in]

Pointer to an instance of <a href="https://msdn.microsoft.com/dafee149-926a-4d08-a43d-5847682db645">IOleClientSite</a>, the primary interface through which the object will request services from its container. This parameter can be <b>NULL</b>.


### -param pStg [in]

Pointer to the <a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> interface for storage for the object. This parameter cannot be <b>NULL</b>.


### -param ppvObj [out]

Address of pointer variable that receives the interface pointer requested in riid. Upon successful return, *<i>ppvObj</i> contains the requested interface pointer on the newly created object.


## -returns



This function returns S_OK on success.




## -remarks



The <b>OleCreateStaticFromData</b> function can convert any object, as long as it provides an <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> interface, to a static object. It is useful in implementing the Convert To Picture option for OLE linking or embedding.



Static objects can be created only if the source supports one of the OLE-rendered clipboard formats: CF_METAFILEPICT, CF_DIB, or CF_ BITMAP, and CF_ENHMETAFILE.



You can also call <b>OleCreateStaticFromData</b> to paste a static object from the clipboard. To determine whether an object is static, call the <a href="https://msdn.microsoft.com/58fffb8c-9726-4801-84ce-6fb670b865c8">OleQueryCreateFromData</a> function, which returns OLE_S_STATIC if one of CF_METAFILEPICT, CF_DIB,  CF_BITMAP, or CF_ENHMETAFILE is present and an OLE format is not present. This indicates that you should call <b>OleCreateStaticFromData</b> rather than the <a href="https://msdn.microsoft.com/aa5e997e-60d4-472d-9c81-5359c277bde3">OleCreateFromData</a> function to create the object.



The new static object is of class CLSID_StaticMetafile in the case of CF_METAFILEPICT, CLSID_StaticDib in the case of CF_DIB or CF_BITMAP, or CLSID_Picture_EnhMetafile in the case of CF_ENHMETAFILE. The static object sets the OLEMISC_STATIC and OLE_CANTLINKINSIDE bits returned from <a href="https://msdn.microsoft.com/0c5e9f73-8eec-48e0-a172-4d3d49e56071">IOleObject::GetMiscStatus</a>. The static object will have the aspect DVASPECT_CONTENT and a LINDEX of -1.

The <i>pSrcDataObject</i> is still valid after <b>OleCreateStaticFromData</b> returns. It is the caller's responsibility to free <i>pSrcDataObject</i> â€” OLE does not release it.



There cannot be more than one presentation stream in a static object.




## -see-also




<a href="https://msdn.microsoft.com/aa5e997e-60d4-472d-9c81-5359c277bde3">OleCreateFromData</a>
 

 

