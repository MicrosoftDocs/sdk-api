---
UID: NF:mfobjects.IMFSample.GetSampleFlags
title: IMFSample::GetSampleFlags (mfobjects.h)
description: Retrieves flags associated with the sample.Currently no flags are defined.
helpviewer_keywords: ["98e3ed97-cefc-40c2-acda-8b3da74d0d03","GetSampleFlags","GetSampleFlags method [Media Foundation]","GetSampleFlags method [Media Foundation]","IMFSample interface","IMFSample interface [Media Foundation]","GetSampleFlags method","IMFSample.GetSampleFlags","IMFSample::GetSampleFlags","mf.imfsample_getsampleflags","mfobjects/IMFSample::GetSampleFlags"]
old-location: mf\imfsample_getsampleflags.htm
tech.root: mf
ms.assetid: 98e3ed97-cefc-40c2-acda-8b3da74d0d03
ms.date: 12/05/2018
ms.keywords: 98e3ed97-cefc-40c2-acda-8b3da74d0d03, GetSampleFlags, GetSampleFlags method [Media Foundation], GetSampleFlags method [Media Foundation],IMFSample interface, IMFSample interface [Media Foundation],GetSampleFlags method, IMFSample.GetSampleFlags, IMFSample::GetSampleFlags, mf.imfsample_getsampleflags, mfobjects/IMFSample::GetSampleFlags
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFSample::GetSampleFlags
 - mfobjects/IMFSample::GetSampleFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFSample.GetSampleFlags
---

# IMFSample::GetSampleFlags


## -description

Retrieves flags associated with the sample.

Currently no flags are defined. Instead, metadata for samples is defined using attributes. To get attributes from a sample, use the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface, which <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a> inherits. For a list of sample attributes, see <a href="/windows/desktop/medfound/sample-attributes">Sample Attributes</a>.

## -parameters

### -param pdwSampleFlags [out]

Receives the value zero.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -remarks

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a>



<a href="/windows/desktop/medfound/media-samples">Media Samples</a>