---
UID: NF:ole2.OleCreate
title: OleCreate function (ole2.h)
description: The OleCreate function (ole2.h) creates an embedded object identified by a CLSID. It can implement the menu item that allows the end user to insert an object.
helpviewer_keywords: ["OleCreate","OleCreate function [COM]","_ole_OleCreate","com.olecreate","ole/OleCreate"]
old-location: com\olecreate.htm
tech.root: com
ms.assetid: 00b7edd2-8e2e-4e0a-91a6-d966f6c8d456
ms.date: 08/15/2022
ms.keywords: OleCreate, OleCreate function [COM], _ole_OleCreate, com.olecreate, ole/OleCreate
req.header: ole2.h
req.include-header: Ole2.h
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
 - OleCreate
 - ole2/OleCreate
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
 - ext-ms-win-com-ole32-l1-1-4.dll
 - ext-ms-win-com-ole32-l1-1-3.dll
 - ext-ms-win-com-ole32-l1-1-2.dll
 - ext-ms-win-com-ole32-l1-1-1.dll
 - ext-ms-win-com-ole32-l1-1-0.dll
 - Ole32.dll
api_name:
 - OleCreate
---

# OleCreate function


## -description

Creates an embedded object identified by a CLSID. You use it typically to implement the menu item that allows the end user to insert a new object.

## -parameters

### -param rclsid [in]

CLSID of the embedded object that is to be created.

### -param riid [in]

Reference to the identifier of the interface, usually IID_IOleObject (defined in the OLE headers as the interface identifier for <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a>), through which the caller will communicate with the new object.

### -param renderopt [in]

A value from the enumeration <a href="/windows/desktop/api/oleidl/ne-oleidl-olerender">OLERENDER</a>, indicating the locally cached drawing capabilities the newly created object is to have. The <b>OLERENDER</b> value chosen affects the possible values for the <i>pFormatEtc</i> parameter.

### -param pFormatEtc [in]

Depending on which of the <a href="/windows/desktop/api/oleidl/ne-oleidl-olerender">OLERENDER</a> flags is used as the value of renderopt, pointer to one of the <a href="/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a> enumeration values. Refer to the <b>OLERENDER</b> enumeration for restrictions. This parameter, along with the <i>renderopt</i> parameter, specifies what the new object can cache initially.

### -param pClientSite [in]

If you want <b>OleCreate</b> to call <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-setclientsite">IOleObject::SetClientSite</a>, pointer to the <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleclientsite">IOleClientSite</a> interface on the container. The value may be <b>NULL</b>, in which case you must specifically call <b>IOleObject::SetClientSite</b> before attempting operations.

### -param pStg [in]

Pointer to an instance of the <a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> interface on the storage object. This parameter may not be <b>NULL</b>.

### -param ppvObj [out]

Address of pointer variable that receives the interface pointer requested in riid. Upon successful return, *<i>ppvObject</i> contains the requested interface pointer.

## -returns

This function returns S_OK on success and supports the standard return value E_OUTOFMEMORY.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory for the operation.

</td>
</tr>
</table>

## -remarks

The <b>OleCreate</b> function creates a new embedded object, and is typically called to implement the menu item Insert New Object. When <b>OleCreate</b> returns, the object it has created is blank (contains no data), unless <i>renderopt</i> is OLERENDER_DRAW or OLERENDER_FORMAT, and is loaded. Containers typically then call the <a href="/windows/desktop/api/ole2/nf-ole2-olerun">OleRun</a> function or <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-doverb">IOleObject::DoVerb</a> to show the object for initial editing.



The <i>rclsid</i> parameter specifies the CLSID of the requested object. CLSIDs of registered objects are stored in the system registry. When an application user selects Insert Object, a selection box allows the user to select the type of object desired from those in the registry. When <b>OleCreate</b> is used to implement the Insert Object menu item, the CLSID associated with the selected item is assigned to the rclsid parameter of <b>OleCreate</b>.



The <i>riid</i> parameter specifies the interface the client will use to communicate with the new object. Upon successful return, the <i>ppvObject</i> parameter holds a pointer to the requested interface.



The created object's cache contains information that allows a presentation of a contained object when the container is opened. Information about what should be cached is passed in the <i>renderopt</i> and <i>pFormatetc</i> values. When <b>OleCreate</b> returns, the created object's cache is not necessarily filled. Instead, the cache is filled the first time the object enters the running state. The caller can add additional cache control with a call to <a href="/windows/desktop/api/oleidl/nf-oleidl-iolecache-cache">IOleCache::Cache</a> after the return of <b>OleCreate</b> and before the object is run. If renderopt is OLERENDER_DRAW or OLERENDER_FORMAT, <b>OleCreate</b> requires that the object support the <a href="/windows/desktop/api/oleidl/nn-oleidl-iolecache">IOleCache</a> interface. There is no such requirement for any other value of renderopt.

If <i>pClientSite</i> is non-<b>NULL</b>, <b>OleCreate</b> calls <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-setclientsite">IOleObject::SetClientSite</a> through the <i>pClientSite</i> pointer. <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleclientsite">IOleClientSite</a> is the primary interface by which an object requests services from its container. If <i>pClientSite</i> is <b>NULL</b>, you must make a specific call to <b>IOleObject::SetClientSite</b> before attempting any operations.

## -see-also

<a href="/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleclientsite">IOleClientSite</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a>



<a href="/windows/desktop/api/oleidl/ne-oleidl-olerender">OLERENDER</a>
