---
UID: NF:ole2.OleConvertOLESTREAMToIStorage
title: OleConvertOLESTREAMToIStorage function (ole2.h)

description: Converts the specified object from the OLE 1 storage model to an OLE 2 structured storage object without specifying presentation data.
old-location: stg\oleconvertolestreamtoistorage.htm
tech.root: Stg
ms.assetid: 8fed879c-5f97-4450-8259-da9643dd828c

ms.date: 12/05/2018
ms.keywords: OleConvertOLESTREAMToIStorage, OleConvertOLESTREAMToIStorage function [Structured Storage], _stg_oleconvertolestreamtoistorage, ole2/OleConvertOLESTREAMToIStorage, stg.oleconvertolestreamtoistorage
ms.topic: function
f1_keywords: 
 - "ole2/OleConvertOLESTREAMToIStorage"
dev_langs:
 - c++
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
 - OleConvertOLESTREAMToIStorage
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# OleConvertOLESTREAMToIStorage function


## -description


The 
<b>OleConvertOLESTREAMToIStorage</b> function converts the specified object from the OLE 1 storage model to an OLE 2 structured storage object without specifying presentation data.
<div class="alert"><b>Note</b>  This is one of several compatibility functions.</div><div> </div>

## -parameters




### -param lpolestream [in]

A pointer to a stream that contains the persistent representation of the object in the OLE 1 storage format.


### -param pstg [out]

A pointer to the 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> interface on the OLE 2 structured storage object.


### -param ptd [in]

A pointer to the 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-dvtargetdevice">DVTARGETDEVICE</a> structure that specifies the target device for which the OLE 1 object is rendered.


## -returns



This function supports the standard return value <b>E_INVALIDARG</b>, in addition to the following:




## -remarks



This function converts an OLE 1 object to an OLE 2 structured storage object. Use this function to update OLE 1 objects to OLE 2 objects when a new version of the object application supports OLE 2.

On entry, the <i>lpolestm</i> parameter should be created and positioned just as it would be for an 
<a href="https://docs.microsoft.com/windows/desktop/api/ole/nf-ole-oleloadfromstream">OleLoadFromStream</a> function call. On exit, the <i>lpolestm</i> parameter is positioned just as it would be on exit from an <b>OleLoadFromStream</b> function, and the <i>pstg</i> parameter contains the uncommitted persistent representation of the OLE 2 storage object.

For OLE 1 objects that use native data for their presentation, the 
<b>OleConvertOLESTREAMToIStorage</b> function returns <b>CONVERT10_S_NO_PRESENTATION</b>. On receiving this return value, callers should call <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleobject-update">IOleObject::Update</a> to get the presentation data so it can be written to storage.

Applications that do not use the OLE default caching resources, but use the conversion resources, can use an alternate function, 
<a href="https://docs.microsoft.com/windows/desktop/api/ole2/nf-ole2-oleconvertolestreamtoistorageex">OleConvertOLESTREAMToIStorageEx</a>, which can specify the presentation data to convert. In the 
<b>OleConvertOLESTREAMToIStorageEx</b> function, the presentation data read from the <b>OLESTREAM</b> structure is passed out and the newly created OLE 2 storage object does not contain a presentation stream.

The following procedure describes the conversion process using 
<b>OleConvertOLESTREAMToIStorage</b>.

<p class="proch"><b>Converting an OLE 1 object to an OLE 2 storage object</b>

<ol>
<li>Create a root 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> object by calling the 
<a href="https://docs.microsoft.com/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile">StgCreateDocfile</a> function (..., &amp;<i>pstg</i>).</li>
<li>Open the OLE 1 file (using <a href="https://docs.microsoft.com/windows/desktop/direct3dtools/ipixengine-openfile-bstr-bstr-inewframescallback-ptr-ifileiocallback-ptr-lcid">OpenFile</a> or another OLE 1 technique).</li>
<li>Read from the file, using the OLE 1 procedure for reading files, until an OLE object is found.</li>
<li>Allocate an 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> object from the root 
<b>IStorage</b> created in Step 1. 



```cpp
pstg->lpVtbl->CreateStorage(...&pStgChild); 
hRes = OleConvertIStorageToOLESTREAM(polestm, pStgChild); 
hRes = OleLoad(pStgChild, &IID_IOleObject, pClientSite, ppvObj);
```


</li>
<li>Repeat Step 3 until the file is completely read.</li>
</ol>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-coisole1class">CoIsOle1Class</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-dvtargetdevice">DVTARGETDEVICE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ole2/nf-ole2-oleconvertistoragetoolestream">OleConvertIStorageToOLESTREAM</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ole2/nf-ole2-oleconvertistoragetoolestreamex">OleConvertIStorageToOLESTREAMEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ole2/nf-ole2-oleconvertolestreamtoistorageex">OleConvertOLESTREAMToIStorageEx</a>



<a href="https://docs.microsoft.com/windows/win32/api/objidl/ns-objidl-ustgmedium~r1">STGMEDIUM</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/ne-objidl-tymed">TYMED</a>
 

 

