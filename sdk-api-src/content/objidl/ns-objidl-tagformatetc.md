---
UID: NS:objidl.tagFORMATETC
title: tagFORMATETC
author: windows-sdk-content
description: Represents a generalized clipboard format.
old-location: com\formatetc.htm
tech.root: com
ms.assetid: 4478eb9a-84a1-4f3a-8290-94b8dd20c081
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: "*LPFORMATETC, FORMATETC, FORMATETC structure [COM], LPFORMATETC, LPFORMATETC structure pointer [COM], _ole_FORMATETC, com.formatetc, objidl/FORMATETC, objidl/LPFORMATETC, tagFORMATETC"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - FORMATETC
product: Windows
targetos: Windows
req.typenames: FORMATETC, *LPFORMATETC
req.redist: 
---

# tagFORMATETC structure


## -description


Represents a generalized clipboard format. It is enhanced to encompass a target device, the aspect or view of the data, and a storage medium indicator. Where one might expect to find a clipboard format, OLE uses a <b>FORMATETC</b> data structure instead. This structure is used as a parameter in OLE functions and methods that require data format information.


## -struct-fields




### -field cfFormat

The clipboard format of interest. There are three types of formats recognized by OLE:


<ul>
<li>Standard interchange formats, such as CF_TEXT.
</li>
<li>Private application formats understood only by the application offering the format, or by other applications offering similar features.
</li>
<li>OLE formats, which are used to create linked or embedded objects.
</li>
</ul>



### -field ptd

A pointer to a <a href="https://msdn.microsoft.com/724ff714-c170-4d06-92cb-e042e41c0af2">DVTARGETDEVICE</a> structure containing information about the target device for which the data is being composed. A <b>NULL</b> value is used whenever the specified data format is independent of the target device or when the caller doesn't care what device is used. In the latter case, if the data requires a target device, the object should pick an appropriate default device (often the display for visual components). Data obtained from an object with a <b>NULL</b> target device, such as most metafiles, is independent of the target device. The resulting data is usually the same as it would be if the user chose the <b>Save As</b> command from the <b>File</b> menu and selected an interchange format.


### -field dwAspect

Indicates how much detail should be contained in the rendering. This parameter should be one of the <a href="https://msdn.microsoft.com/a2b729c8-7091-4520-93cd-c44468ba0274">DVASPECT</a> enumeration values. A single clipboard format can support multiple aspects or views of the object. Most data and presentation transfer and caching methods pass aspect information. For example, a caller might request an object's iconic picture, using the metafile clipboard format to retrieve it. Note that only one <b>DVASPECT</b> value can be used in <b>dwAspect</b>. That is, <b>dwAspect</b> cannot be the result of a Boolean OR operation on several <b>DVASPECT</b> values.


### -field lindex

Part of the aspect when the data must be split across page boundaries. The most common value is -1, which identifies all of the data. For the aspects DVASPECT_THUMBNAIL and DVASPECT_ICON, lindex is ignored.


### -field tymed

One of the <a href="https://msdn.microsoft.com/ac41286f-7c67-444a-81b7-21b61079bbf5">TYMED</a> enumeration constants which indicate the type of storage medium used to transfer the object's data. Data can be transferred using whatever medium makes sense for the object. For example, data can be passed using global memory, a disk file, or structured storage objects. For more information, see the <b>TYMED</b> enumeration.


## -remarks



The <b>FORMATETC</b> structure is used by methods in the data transfer and presentation interfaces as a parameter specifying the data being transferred. For example, the <a href="https://msdn.microsoft.com/05118461-0438-4715-b2c2-fc2471ce38f0">IDataObject::GetData</a> method uses the <b>FORMATETC</b> structure to indicate exactly what kind of data the caller is requesting.




## -see-also




<a href="https://msdn.microsoft.com/a2b729c8-7091-4520-93cd-c44468ba0274">DVASPECT</a>



<a href="https://msdn.microsoft.com/740a6366-6ab1-4a20-82df-1efdd62211eb">IDataAdviseHolder</a>



<a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>



<a href="https://msdn.microsoft.com/4d180fdd-2d58-4d26-9242-6552dda0d3e6">IEnumFORMATETC</a>



<a href="https://msdn.microsoft.com/b5ef85d0-b54e-4831-87f1-ac6763179181">IOleCache</a>



<a href="https://msdn.microsoft.com/00b7edd2-8e2e-4e0a-91a6-d966f6c8d456">OleCreate</a>



<a href="https://msdn.microsoft.com/aa5e997e-60d4-472d-9c81-5359c277bde3">OleCreateFromData</a>



<a href="https://msdn.microsoft.com/ef52dc37-aa63-47f3-a04f-f9d22178690f">OleCreateLink</a>



<a href="https://msdn.microsoft.com/3eda0cf5-c33d-43cf-ba8a-02a4f6383adc">OleCreateLinkFromData</a>



<a href="https://msdn.microsoft.com/06b013db-0554-4dbc-b19d-28314fb4fee0">OleCreateLinkToFile</a>



<a href="https://msdn.microsoft.com/847d82f5-149d-48a4-a228-f5551a07a790">OleCreateStaticFromData</a>



<a href="https://msdn.microsoft.com/f31469b2-4a4a-4da5-9229-38ddd0bcc88e">STATDATA</a>



<a href="https://msdn.microsoft.com/5d05819a-10db-4d8e-91e4-8a7c05885cde">STGMEDIUM</a>



<a href="https://msdn.microsoft.com/ac41286f-7c67-444a-81b7-21b61079bbf5">TYMED</a>
 

 

