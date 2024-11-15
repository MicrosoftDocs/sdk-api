---
UID: NF:ole2.OleCreateFromFileEx
title: OleCreateFromFileEx function (ole2.h)
description: Extends OleCreateFromFile functionality by supporting more efficient instantiation of objects in containers requiring caching of multiple presentation formats or data, instead of the single format supported by OleCreateFromFile.
helpviewer_keywords: ["OleCreateFromFileEx","OleCreateFromFileEx function [COM]","_ole_OleCreateFromFileEx","com.olecreatefromfileex","ole2/OleCreateFromFileEx"]
old-location: com\olecreatefromfileex.htm
tech.root: com
ms.assetid: a75bb031-6e4a-4440-82f3-6a6f9417c62b
ms.date: 12/05/2018
ms.keywords: OleCreateFromFileEx, OleCreateFromFileEx function [COM], _ole_OleCreateFromFileEx, com.olecreatefromfileex, ole2/OleCreateFromFileEx
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
 - OleCreateFromFileEx
 - ole2/OleCreateFromFileEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
api_name:
 - OleCreateFromFileEx
---

# OleCreateFromFileEx function


## -description

Extends <a href="/windows/desktop/api/ole/nf-ole-olecreatefromfile">OleCreateFromFile</a> functionality by supporting more efficient instantiation of objects in containers requiring caching of multiple presentation formats or data, instead of the single format supported by <b>OleCreateFromFile</b>.

## -parameters

### -param rclsid [in]

This parameter is reserved and must be CLSID_NULL.

### -param lpszFileName [in]

Pointer to the name of the file from which the new object should be initialized.

### -param riid [in]

Reference to the identifier of the interface of the object to return.

### -param dwFlags [in]

This parameter can be 0 or OLECREATE_LEAVERUNNING (0x00000001).

### -param renderopt [in]

Value taken from the <a href="/windows/desktop/api/oleidl/ne-oleidl-olerender">OLERENDER</a> enumeration.

### -param cFormats [in]

When <i>renderopt</i> is OLERENDER_FORMAT, indicates the number of <a href="/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a> structures in the <i>rgFormatEtc</i> array, which must be at least one. In all other cases, this parameter must be zero.

### -param rgAdvf [in]

When <i>renderopt</i> is OLERENDER_FORMAT, points to an array of <b>DWORD</b> elements, each of which is a combination of values from the <a href="/windows/desktop/api/objidl/ne-objidl-advf">ADVF</a> enumeration. Each element of this array is passed in as the <i>advf</i> parameter to a call to either <a href="/windows/desktop/api/oleidl/nf-oleidl-iolecache-cache">IOleCache::Cache</a> or <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-dadvise">IDataObject::DAdvise</a>, depending on whether <i>pAdviseSink</i> is <b>NULL</b> or non-<b>NULL</b> (see below). In all other cases, this parameter must be <b>NULL</b>.

### -param rgFormatEtc [in]

When <i>renderopt</i> is OLERENDER_FORMAT, points to an array of <a href="/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a> structures. When <i>pAdviseSink</i> is <b>NULL</b>, each element of this array is passed as the <i>pFormatEtc</i> parameter to a call to the object's <a href="/windows/desktop/api/oleidl/nf-oleidl-iolecache-cache">IOleCache::Cache</a>. This populates the data and presentation cache managed by the objects in-process handler (typically the default handler) with presentation or other cacheable data. When <i>pAdviseSink</i> is non-<b>NULL</b>, each element of this array is passed as the <i>pFormatEtc</i> parameter to a call to <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-dadvise">IDataObject::DAdvise</a>. This allows the caller (typically an OLE Container) to do its own caching or processing of data received from the object.

### -param lpAdviseSink [in]

When <i>renderopt</i> is OLERENDER_FORMAT, may be either a valid <a href="/windows/desktop/api/objidl/nn-objidl-iadvisesink">IAdviseSink</a> pointer, indicating custom caching or processing of data advises, or <b>NULL</b>, indicating default caching of data formats.

### -param rgdwConnection [out]

Location to return the array of <i>dwConnection</i> values returned when the <i>pAdviseSink</i> interface is registered for each advisory connection using <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-dadvise">IDataObject::DAdvise</a>, or <b>NULL</b> if the returned advisory connections are not needed. This parameter must be <b>NULL</b> if <i>pAdviseSink</i> is <b>NULL</b>.

### -param pClientSite [in]

Pointer to the primary interface through which the object will request services from its container. This parameter may be <b>NULL</b>, in which case it is the caller's responsibility to establish the client site as soon as possible using <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-setclientsite">IOleObject::SetClientSite</a>.

### -param pStg [in]

Pointer to the storage to use for the object and any default data or presentation caching established for it.

### -param ppvObj [out]

Address of output pointer variable that receives the interface pointer requested in riid. Upon successful return, *<i>ppvObj</i> contains the requested interface pointer on the newly created object.

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
The provided interface identifier is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG </b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
</table>

## -remarks

The following call to <a href="/windows/desktop/api/ole/nf-ole-olecreatefromfile">OleCreateFromFile</a>:


``` syntax
OleCreateFromFile(rclsid, lpszFileName, riid, renderopt, pFormatEtc, pClientSite, pStg, ppvObj);
```

is equivalent to the following call to <b>OleCreateFromFileEx</b>:




``` syntax
DWORD    advf = ADVF_PRIMEFIRST;
    OleCreateFromFileEx(rclsid, lpszFileName, riid, renderopt, 1, &advf, pFormatEtc, NULL, pClientSite, pStg, ppvObj);
```

Existing instantiation functions (<a href="/windows/desktop/api/ole/nf-ole-olecreate">OleCreate</a>, <a href="/windows/desktop/api/ole/nf-ole-olecreatefromfile">OleCreateFromFile</a>, <a href="/windows/desktop/api/ole2/nf-ole2-olecreatefromdata">OleCreateFromData</a>, <a href="/windows/desktop/api/ole2/nf-ole2-olecreatelink">OleCreateLink</a>, <a href="/windows/desktop/api/ole2/nf-ole2-olecreatelinktofile">OleCreateLinkToFile</a>, and <a href="/windows/desktop/api/ole2/nf-ole2-olecreatelinkfromdata">OleCreateLinkFromData</a>) create only a single presentation or data format cache in the default cache location (within the '\001OlePresXXX' streams of the passed-in <a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a>), during instantiation. Plus, these caches must be created when the object next enters the running state. Because most applications require caching at least two presentations (screen and printer) and may require caching data in a different format or location from the handler, applications must typically launch and shut down the object server multiple times in order to prime their data caches during object creation, i.e., Insert Object, Insert Object from File, and Paste Object.

Extended versions of these creation functions solve this problem. <a href="/windows/desktop/api/ole2/nf-ole2-olecreateex">OleCreateEx</a>, <b>OleCreateFromFileEx</b>, <a href="/windows/desktop/api/ole2/nf-ole2-olecreatefromdataex">OleCreateFromDataEx</a>, <a href="/windows/desktop/api/ole2/nf-ole2-olecreatelinkex">OleCreateLinkEx</a>, <a href="/windows/desktop/api/ole2/nf-ole2-olecreatelinktofileex">OleCreateLinkToFileEx</a>, and <a href="/windows/desktop/api/ole2/nf-ole2-olecreatelinkfromdataex">OleCreateLinkFromDataEx</a>, contain the following new parameters: <i>dwFlags</i> to indicate additional options, <i>cFormats</i> to indicate how many formats to cache, <i>rgAdvf</i>, from the <a href="/windows/desktop/api/objidl/ne-objidl-advf">ADVF</a> enumeration, to specify the advise flags for each format to be cached, <i>pAdviseSink</i> to indicate whether presentation (default-handler) or data (non-default-handler) caching is required, <i>rgdwConnection</i> to return <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-dadvise">IDataObject::DAdvise</a> cookies, and <i>rgFormatEtc</i>, an array of formats rather than a single format.

Containers requiring that multiple presentations be cached on their behalf by the object's handler can simply call these functions and specify the number of formats in <i>cFormats</i>, the <a href="/windows/desktop/api/objidl/ne-objidl-advf">ADVF</a> flags for each format in <i>rgAdvf</i>, and the set of formats in <i>rgFormatEtc</i>. These containers pass <b>NULL</b> for <i>pAdviseSink</i>.

Containers performing all their own data- or presentation-caching perform these same steps, but pass a non-<b>NULL</b><i>pAdviseSink</i>. They perform their own caching or manipulation of the object or data during <a href="/windows/desktop/api/objidl/nf-objidl-iadvisesink-ondatachange">IAdviseSink::OnDataChange</a>. Typically, such containers never establish the advisory connections with ADVF_NODATA, although they are not prevented from doing so.

These new functions are for OLE Compound Documents. Using these functions, applications can avoid the repeated launching and initialization steps required by the current functions. They are targeted at OLE Compound Document container applications that use default data- and presentation-caching, and also at applications that provide their own caching and data transfer from the underlying <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-dadvise">IDataObject::DAdvise</a> support.

## -see-also

<a href="/windows/desktop/api/objidl/ne-objidl-advf">ADVF</a>



<a href="/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a>



<a href="/windows/desktop/api/objidl/nf-objidl-iadvisesink-ondatachange">IAdviseSink::OnDataChange</a>



<a href="/windows/desktop/api/objidl/nf-objidl-idataobject-dadvise">IDataObject::DAdvise</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-iolecache-cache">IOleCache::Cache</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-setclientsite">IOleObject::SetClientSite</a>



<a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a>



<a href="/windows/desktop/api/oleidl/ne-oleidl-olerender">OLERENDER</a>



<a href="/windows/desktop/api/ole/nf-ole-olecreatefromfile">OleCreateFromFile</a>
