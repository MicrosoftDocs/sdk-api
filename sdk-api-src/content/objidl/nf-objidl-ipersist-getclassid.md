---
UID: NF:objidl.IPersist.GetClassID
title: IPersist::GetClassID (objidl.h)
description: Retrieves the class identifier (CLSID) of the object.
helpviewer_keywords: ["GetClassID","GetClassID method [COM]","GetClassID method [COM]","IBaseFilter interface","GetClassID method [COM]","IPersist interface","GetClassID method [COM]","IPersistFolder interface","IBaseFilter interface [COM]","GetClassID method","IBaseFilter::GetClassID","IPersist interface [COM]","GetClassID method","IPersist.GetClassID","IPersist::GetClassID","IPersistFolder interface [COM]","GetClassID method","IPersistFolder::GetClassID","_com_ipersist_getclassid","com.ipersist_getclassid","objidl/IBaseFilter::GetClassID","objidl/IPersist::GetClassID","objidl/IPersistFolder::GetClassID"]
old-location: com\ipersist_getclassid.htm
tech.root: com
ms.assetid: 921a3b86-a240-454e-9411-8d653e02b90e
ms.date: 12/05/2018
ms.keywords: GetClassID, GetClassID method [COM], GetClassID method [COM],IBaseFilter interface, GetClassID method [COM],IPersist interface, GetClassID method [COM],IPersistFolder interface, IBaseFilter interface [COM],GetClassID method, IBaseFilter::GetClassID, IPersist interface [COM],GetClassID method, IPersist.GetClassID, IPersist::GetClassID, IPersistFolder interface [COM],GetClassID method, IPersistFolder::GetClassID, _com_ipersist_getclassid, com.ipersist_getclassid, objidl/IBaseFilter::GetClassID, objidl/IPersist::GetClassID, objidl/IPersistFolder::GetClassID
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPersist::GetClassID
 - objidl/IPersist::GetClassID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IPersist.GetClassID
 - IPersistFolder.GetClassID
 - IBaseFilter.GetClassID
---

# IPersist::GetClassID


## -description

Retrieves the class identifier (CLSID) of the object.

## -parameters

### -param pClassID [out]

A pointer to the location that receives the CLSID on return. The CLSID is a globally unique identifier (GUID) that uniquely represents an object class that defines the code that can manipulate the object's data.

## -returns

If the method succeeds, the return value is S_OK. Otherwise, it is E_FAIL.

## -remarks

The <b>GetClassID</b> method retrieves the class identifier (CLSID) for an object, used in later operations to load object-specific code into the caller's context.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
A container application might call this method to retrieve the original CLSID of an object that it is treating as a different class. Such a call would be necessary if a user performed an editing operation that required the object to be saved. If the container were to save it using the treat-as CLSID, the original application would no longer be able to edit the object. Typically, in this case, the container calls the <a href="/windows/desktop/api/ole2/nf-ole2-olesave">OleSave</a> helper function, which performs all the necessary steps. For this reason, most container applications have no need to call this method directly.

The exception would be a container that provides an object handler for certain objects. In particular, a container application should not get an object's CLSID and then use it to retrieve class specific information from the registry. Instead, the container should use <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a> and <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> interfaces to retrieve such class-specific information directly from the object.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Typically, implementations of this method simply supply a constant CLSID for an object. If, however, the object's <b><a href="/windows/desktop/com/treatas">TreatAs</a></b> registry key has been set by an application that supports emulation (and so is treating the object as one of a different class), a call to <b>GetClassID</b> must supply the CLSID specified in the <b><a href="/windows/desktop/com/treatas">TreatAs</a></b> key. For more information on emulation, see <a href="/windows/desktop/api/objbase/nf-objbase-cotreatasclass">CoTreatAsClass</a>.

When an object is in the running state, the default handler calls an implementation of <b>GetClassID</b> that delegates the call to the implementation in the object. When the object is not running, the default handler instead calls the <a href="/windows/desktop/api/coml2api/nf-coml2api-readclassstg">ReadClassStg</a> function to read the CLSID that is saved in the object's storage.

If you are writing a custom object handler for your object, you might want to simply delegate this method to the default handler implementation (see <a href="/windows/desktop/api/ole2/nf-ole2-olecreatedefaulthandler">OleCreateDefaultHandler</a>). 


<h3><a id="URL_Moniker_Notes"></a><a id="url_moniker_notes"></a><a id="URL_MONIKER_NOTES"></a>URL Moniker Notes</h3>
This method returns CLSID_StdURLMoniker.

## -see-also

<a href="/windows/desktop/api/strmif/nn-strmif-ibasefilter">IBaseFilter</a>



<a href="/windows/desktop/api/objidl/nn-objidl-ipersist">IPersist</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder">IPersistFolder</a>