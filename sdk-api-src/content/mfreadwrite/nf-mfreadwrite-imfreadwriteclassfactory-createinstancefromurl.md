---
UID: NF:mfreadwrite.IMFReadWriteClassFactory.CreateInstanceFromURL
title: IMFReadWriteClassFactory::CreateInstanceFromURL (mfreadwrite.h)
description: Creates an instance of the sink writer or source reader, given a URL.
helpviewer_keywords: ["CLSID_MFSinkWriter","CLSID_MFSourceReader","CreateInstanceFromURL","CreateInstanceFromURL method [Media Foundation]","CreateInstanceFromURL method [Media Foundation]","IMFReadWriteClassFactory interface","IMFReadWriteClassFactory interface [Media Foundation]","CreateInstanceFromURL method","IMFReadWriteClassFactory.CreateInstanceFromURL","IMFReadWriteClassFactory::CreateInstanceFromURL","mf.imfreadwriteclassfactory_createinstancefromurl","mfreadwrite/IMFReadWriteClassFactory::CreateInstanceFromURL"]
old-location: mf\imfreadwriteclassfactory_createinstancefromurl.htm
tech.root: mf
ms.assetid: 2769faa2-e381-4908-95f8-122ae4cd7ec5
ms.date: 12/05/2018
ms.keywords: CLSID_MFSinkWriter, CLSID_MFSourceReader, CreateInstanceFromURL, CreateInstanceFromURL method [Media Foundation], CreateInstanceFromURL method [Media Foundation],IMFReadWriteClassFactory interface, IMFReadWriteClassFactory interface [Media Foundation],CreateInstanceFromURL method, IMFReadWriteClassFactory.CreateInstanceFromURL, IMFReadWriteClassFactory::CreateInstanceFromURL, mf.imfreadwriteclassfactory_createinstancefromurl, mfreadwrite/IMFReadWriteClassFactory::CreateInstanceFromURL
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
 - IMFReadWriteClassFactory::CreateInstanceFromURL
 - mfreadwrite/IMFReadWriteClassFactory::CreateInstanceFromURL
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
 - IMFReadWriteClassFactory.CreateInstanceFromURL
---

# IMFReadWriteClassFactory::CreateInstanceFromURL


## -description

Creates an instance of the sink writer or source reader, given a URL.

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

### -param pwszURL [in]

A null-terminated string that contains a URL. If <i>clsid</i> is CLSID_<b>MFSinkWriter</b>, the URL specifies the name of the output file. The sink writer creates a new file with this name. If <i>clsid</i> is <b>CLSID_MFSourceReader</b>, the URL specifies the input file for the source reader.

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