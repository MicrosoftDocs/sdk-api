---
UID: NF:mfreadwrite.IMFReadWriteClassFactory.CreateInstanceFromObject
title: IMFReadWriteClassFactory::CreateInstanceFromObject (mfreadwrite.h)
description: Creates an instance of the sink writer or source reader, given an IUnknown pointer.
helpviewer_keywords: ["CLSID_MFSinkWriter","CLSID_MFSourceReader","CreateInstanceFromObject","CreateInstanceFromObject method [Media Foundation]","CreateInstanceFromObject method [Media Foundation]","IMFReadWriteClassFactory interface","IMFByteStream","IMFMediaSink","IMFMediaSource","IMFReadWriteClassFactory interface [Media Foundation]","CreateInstanceFromObject method","IMFReadWriteClassFactory.CreateInstanceFromObject","IMFReadWriteClassFactory::CreateInstanceFromObject","mf.imfreadwriteclassfactory_createinstancefromobject","mfreadwrite/IMFReadWriteClassFactory::CreateInstanceFromObject"]
old-location: mf\imfreadwriteclassfactory_createinstancefromobject.htm
tech.root: mf
ms.assetid: 5da582c2-37f9-47ee-b8ea-d21f1323f1df
ms.date: 12/05/2018
ms.keywords: CLSID_MFSinkWriter, CLSID_MFSourceReader, CreateInstanceFromObject, CreateInstanceFromObject method [Media Foundation], CreateInstanceFromObject method [Media Foundation],IMFReadWriteClassFactory interface, IMFByteStream, IMFMediaSink, IMFMediaSource, IMFReadWriteClassFactory interface [Media Foundation],CreateInstanceFromObject method, IMFReadWriteClassFactory.CreateInstanceFromObject, IMFReadWriteClassFactory::CreateInstanceFromObject, mf.imfreadwriteclassfactory_createinstancefromobject, mfreadwrite/IMFReadWriteClassFactory::CreateInstanceFromObject
req.header: mfreadwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista and Platform Update Supplement for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFReadWriteClassFactory::CreateInstanceFromObject
 - mfreadwrite/IMFReadWriteClassFactory::CreateInstanceFromObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfreadwrite.h
api_name:
 - IMFReadWriteClassFactory.CreateInstanceFromObject
---

# IMFReadWriteClassFactory::CreateInstanceFromObject


## -description

Creates an instance of the sink writer or source reader, given an <b>IUnknown</b> pointer.

## -parameters

### -param clsid [in]

The CLSID of the object to create.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CLSID_MFSinkWriter"></a><a id="clsid_mfsinkwriter"></a><a id="CLSID_MFSINKWRITER"></a><dl>
<dt><b>CLSID_MFSinkWriter</b></dt>
</dl>
</td>
<td width="60%">
Create the sink writer. The <i>ppvObject</i> parameter receives an <a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter">IMFSinkWriter</a> interface pointer.

</td>
</tr>
<tr>
<td width="40%"><a id="CLSID_MFSourceReader"></a><a id="clsid_mfsourcereader"></a><a id="CLSID_MFSOURCEREADER"></a><dl>
<dt><b>CLSID_MFSourceReader</b></dt>
</dl>
</td>
<td width="60%">
Create the source reader. The <i>ppvObject</i> parameter receives an <a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader">IMFSourceReader</a> interface pointer.

</td>
</tr>
</table>

### -param punkObject [in]

A pointer to the <b>IUnknown</b> interface of an object that is used to initialize the source reader or sink writer. The method queries this pointer for one of the following interfaces.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IMFByteStream"></a><a id="imfbytestream"></a><a id="IMFBYTESTREAM"></a><dl>
<dt><b><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a></b></dt>
</dl>
</td>
<td width="60%">
Pointer to a byte stream. 

If <i>clsid</i> is <b>CLSID_MFSinkWriter</b>, the sink writer writes data to this byte stream.

If <i>clsid</i> is <b>CLSID_MFSourceReader</b>, this byte stream provides the source data for the source reader.

</td>
</tr>
<tr>
<td width="40%"><a id="IMFMediaSink"></a><a id="imfmediasink"></a><a id="IMFMEDIASINK"></a><dl>
<dt><b><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasink">IMFMediaSink</a></b></dt>
</dl>
</td>
<td width="60%">
Pointer to a media sink. Applies only when <i>clsid</i> is <b>CLSID_MFSinkWriter</b>. 

</td>
</tr>
<tr>
<td width="40%"><a id="IMFMediaSource"></a><a id="imfmediasource"></a><a id="IMFMEDIASOURCE"></a><dl>
<dt><b><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasource">IMFMediaSource</a></b></dt>
</dl>
</td>
<td width="60%">
Pointer to a media source. Applies only when <i>clsid</i> is <b>CLSID_MFSourceReader</b>.

</td>
</tr>
</table>

### -param pAttributes [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface. You can use this parameter to configure the sink writer or source reader. For more information, see the following topics:

<ul>
<li>
<a href="/windows/desktop/medfound/sink-writer-attributes">Sink Writer Attributes</a>
</li>
<li>
<a href="/windows/desktop/medfound/source-reader-attributes">Source Reader Attributes</a>
</li>
</ul>
This parameter can be <b>NULL</b>.

### -param riid [in]

The IID of the requested interface.

### -param ppvObject [out]

Receives a pointer to the requested interface. The caller must release the interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.

## -see-also

<a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfreadwriteclassfactory">IMFReadWriteClassFactory</a>