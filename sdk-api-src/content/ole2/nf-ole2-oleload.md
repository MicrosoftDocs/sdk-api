---
UID: NF:ole2.OleLoad
title: OleLoad function (ole2.h)
description: Loads into memory an object nested within a specified storage object.
helpviewer_keywords: ["OleLoad","OleLoad function [COM]","_ole_OleLoad","com.oleload","ole2/OleLoad"]
old-location: com\oleload.htm
tech.root: com
ms.assetid: f2d8bb2e-5bd1-4991-a80c-ed06bfd5c9f9
ms.date: 12/05/2018
ms.keywords: OleLoad, OleLoad function [COM], _ole_OleLoad, com.oleload, ole2/OleLoad
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
 - OleLoad
 - ole2/OleLoad
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
 - OleLoad
---

# OleLoad function


## -description

Loads into memory an object nested within a specified storage object.

## -parameters

### -param pStg [in]

Pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> interface on the storage object from which to load the specified object.

### -param riid [in]

Reference to the identifier of the interface that the caller wants to use to communicate with the object after it is loaded.

### -param pClientSite [in]

Pointer to the <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleclientsite">IOleClientSite</a> interface on the client site object being loaded.

### -param ppvObj [out]

Address of pointer variable that receives the interface pointer requested in riid. Upon successful return, *<i>ppvObj</i> contains the requested interface pointer on the newly loaded object.

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
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The object does not support the specified interface.

</td>
</tr>
</table>
 

Additionally, this function can return any of the error values returned by the <a href="/windows/desktop/api/objidl/nf-objidl-ipersiststorage-load">IPersistStorage::Load</a> method.

## -remarks

OLE containers load objects into memory by calling this function. When calling the <b>OleLoad</b> function, the container application passes in a pointer to the open storage object in which the nested object is stored. Typically, the nested object to be loaded is a child storage object to the container's root storage object. Using the OLE information stored with the object, the object handler (usually, the default handler) attempts to load the object. On completion of the <b>OleLoad</b> function, the object is said to be in the loaded state with its object application not running.

Some applications load all of the object's native data. Containers often defer loading the contained objects until required to do so. For example, until an object is scrolled into view and needs to be drawn, it does not need to be loaded.

The <b>OleLoad</b> function performs the following steps:

<ul>
<li>If necessary, performs an automatic conversion of the object (see the <a href="/windows/desktop/api/ole2/nf-ole2-oledoautoconvert">OleDoAutoConvert</a> function).</li>
<li>Gets the CLSID from the open storage object by calling the <a href="/windows/desktop/api/objidl/nf-objidl-istorage-stat">IStorage::Stat</a> method.</li>
<li> Calls the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> function to create an instance of the handler. If the handler code is not available, the default handler is used (see the <a href="/windows/desktop/api/ole2/nf-ole2-olecreatedefaulthandler">OleCreateDefaultHandler</a> function).</li>
<li>Calls the <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-setclientsite">IOleObject::SetClientSite</a> method with the <i>pClientSite</i> parameter to inform the object of its client site.</li>
<li>Calls the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method for the <a href="/windows/desktop/api/objidl/nn-objidl-ipersiststorage">IPersistStorage</a> interface. If successful, the <a href="/windows/desktop/api/objidl/nf-objidl-ipersiststorage-load">IPersistStorage::Load</a> method is invoked for the object.</li>
<li>Queries and returns the interface identified by the <i>riid</i> parameter.</li>
</ul>