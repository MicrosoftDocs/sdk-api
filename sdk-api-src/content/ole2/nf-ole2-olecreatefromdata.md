---
UID: NF:ole2.OleCreateFromData
title: OleCreateFromData function (ole2.h)
description: Creates an embedded object from a data transfer object retrieved either from the clipboard or as part of an OLE drag-and-drop operation. It is intended to be used to implement a paste from an OLE drag-and-drop operation.
helpviewer_keywords: ["OleCreateFromData","OleCreateFromData function [COM]","_ole_OleCreateFromData","com.olecreatefromdata","ole2/OleCreateFromData"]
old-location: com\olecreatefromdata.htm
tech.root: com
ms.assetid: aa5e997e-60d4-472d-9c81-5359c277bde3
ms.date: 12/05/2018
ms.keywords: OleCreateFromData, OleCreateFromData function [COM], _ole_OleCreateFromData, com.olecreatefromdata, ole2/OleCreateFromData
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - OleCreateFromData
 - ole2/OleCreateFromData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-com-ole32-l1-4-0.dll
 - ext-ms-win-com-ole32-l1-3-0.dll
 - ext-ms-win-com-ole32-l1-2-0.dll
 - ext-ms-win-com-ole32-l1-1-5.dll
 - Ole32.dll
 - ext-ms-win-com-ole32-l1-1-3.dll
 - Ext-MS-Win-Com-Ole32-L1-1-4.dll
api_name:
 - OleCreateFromData
req.apiset: ext-ms-win-com-ole32-l1-1-3 (introduced in Windows 10, version 10.0.10240)
---

# OleCreateFromData function


## -description

Creates an embedded object from a data transfer object retrieved either from the clipboard or as part of an OLE drag-and-drop operation. It is intended to be used to implement a paste from an OLE drag-and-drop operation.

## -parameters

### -param pSrcDataObj [in]

Pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> interface on the data transfer object that holds the data from which the object is created.

### -param riid [in]

Reference to the identifier of the interface the caller later uses to communicate with the new object (usually IID_IOleObject, defined in the OLE headers as the interface identifier for <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a>).

### -param renderopt [in]

Value from the enumeration <a href="/windows/desktop/api/oleidl/ne-oleidl-olerender">OLERENDER</a> that indicates the locally cached drawing or data-retrieval capabilities the newly created object is to have. Additional considerations are described in the following Remarks section.

### -param pFormatEtc [in]

 Pointer to a value from the enumeration <a href="/windows/desktop/api/oleidl/ne-oleidl-olerender">OLERENDER</a> that indicates the locally cached drawing or data-retrieval capabilities the newly created object is to have. The <b>OLERENDER</b> value chosen affects the possible values for the <i>pFormatEtc</i> parameter.

### -param pClientSite [in]

Pointer to an instance of <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleclientsite">IOleClientSite</a>, the primary interface through which the object will request services from its container. This parameter can be <b>NULL</b>.

### -param pStg [in]

Pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> interface on the storage object. This parameter may not be <b>NULL</b>.

### -param ppvObj [out]

Address of pointer variable that receives the interface pointer requested in riid. Upon successful return, *<i>ppvObj</i> contains the requested interface pointer on the newly created object.

## -returns

This function returns S_OK on success. Other possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_STATIC</b></dt>
</dl>
</td>
<td width="60%">
Indicates OLE can create only a static object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DV_E_FORMATETC</b></dt>
</dl>
</td>
<td width="60%">
No acceptable formats are available for object creation.

</td>
</tr>
</table>

## -remarks

The <b>OleCreateFromData</b> function creates an embedded object from a data transfer object supporting the <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> interface. The data object in this case is either the type retrieved from the clipboard with a call to the <a href="/windows/desktop/api/ole2/nf-ole2-olegetclipboard">OleGetClipboard</a> function or is part of an OLE drag-and-drop operation (the data object is passed to a call to <a href="/windows/desktop/api/oleidl/nf-oleidl-idroptarget-drop">IDropTarget::Drop</a>).

If either the FileName or FileNameW clipboard format (CF_FILENAME) is present in the data transfer object, and CF_EMBEDDEDOBJECT or CF_EMBEDSOURCE do not exist, <b>OleCreateFromData</b> first attempts to create a package containing the indicated file. Generally, it takes the first available format. 

If <b>OleCreateFromData</b> cannot create a package, it tries to create an object using the CF_EMBEDDEDOBJECT format. If that format is not available, <b>OleCreateFromData</b> tries to create it with the CF_EMBEDSOURCE format. If neither of these formats is available and the data transfer object supports the <a href="/windows/desktop/api/objidl/nn-objidl-ipersiststorage">IPersistStorage</a> interface, <b>OleCreateFromData</b> calls the object's <a href="/windows/desktop/api/objidl/nf-objidl-ipersiststorage-save">IPersistStorage::Save</a> to have the object save itself.



If an existing linked object is selected, then copied, it appears on the clipboard as just another embeddable object. Consequently, a paste operation that invokes <b>OleCreateFromData</b> may create a linked object. After the paste operation, the container should call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> function, requesting IID_IOleLink (defined in the OLE headers as the interface identifier for <a href="/windows/desktop/api/oleidl/nn-oleidl-iolelink">IOleLink</a>), to determine if a linked object was created.



Use the <i>renderopt</i> and <i>pFormatetc</i> parameters to control the caching capability of the newly created object. For general information about using the interaction of these parameters to determine what is to be cached, refer to the <a href="/windows/desktop/api/oleidl/ne-oleidl-olerender">OLERENDER</a> enumeration. There are, however, some additional specific effects of these parameters on the way <b>OleCreateFromData</b> initializes the cache.



When <b>OleCreateFromData</b> uses either the CF_EMBEDDEDOBJECT or the CF_EMBEDSOURCE clipboard format to create the embedded object, the main difference between the two is where the cache-initialization data is stored: 



<ul>
<li>CF_EMBEDDEDOBJECT indicates that the source is an existing embedded object. It already has in its cache the appropriate data, and OLE uses this data to initialize the cache of the new object. 
</li>
<li>CF_EMBEDSOURCE indicates that the source data object contains the cache-initialization information in formats other than CF_EMBEDSOURCE. <b>OleCreateFromData</b> uses these to initialize the cache of the newly embedded object. </li>
</ul>
The <i>renderopt</i> values affect cache initialization as follows.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>
OLERENDER_DRAW &amp; OLERENDER_FORMAT


</td>
<td>
If the presentation information to be cached is currently present in the appropriate cache-initialization pool, it is used. (Appropriate locations are in the source data object cache for CF_EMBEDDEDOBJECT, and in the other formats in the source data object for CF_EMBEDSOURCE.) If the information is not present, the cache is initially empty, but will be filled the first time the object is run. No other formats are cached in the newly created object.


</td>
</tr>
<tr>
<td>
OLERENDER_NONE


</td>
<td>
Nothing is to be cached in the newly created object. If the source has the CF_EMBEDDEDOBJECT format, any existing cached data that has been copied is removed.


</td>
</tr>
<tr>
<td>
OLERENDER_ASIS


</td>
<td>
If the source has the CF_EMBEDDEDOBJECT format, the cache of the new object is to contain the same cache data as the source object. For CF_EMBEDSOURCE, nothing is to be cached in the newly created object. This option should be used by more sophisticated containers. After this call, such containers would call <a href="/windows/desktop/api/oleidl/nf-oleidl-iolecache-cache">IOleCache::Cache</a> and <a href="/windows/desktop/api/oleidl/nf-oleidl-iolecache-uncache">IOleCache::Uncache</a> to set up exactly what is to be cached. For CF_EMBEDSOURCE, they would then also call <a href="/windows/desktop/api/oleidl/nf-oleidl-iolecache-initcache">IOleCache::InitCache</a>.


</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>



<a href="/windows/desktop/api/ole/nf-ole-olecreate">OleCreate</a>
