---
UID: NF:mfobjects.IMFSample.SetSampleFlags
title: IMFSample::SetSampleFlags (mfobjects.h)
description: Sets flags associated with the sample.Currently no flags are defined.
helpviewer_keywords: ["30dac293-981b-41f3-951d-186d6a603d0a","IMFSample interface [Media Foundation]","SetSampleFlags method","IMFSample.SetSampleFlags","IMFSample::SetSampleFlags","SetSampleFlags","SetSampleFlags method [Media Foundation]","SetSampleFlags method [Media Foundation]","IMFSample interface","mf.imfsample_setsampleflags","mfobjects/IMFSample::SetSampleFlags"]
old-location: mf\imfsample_setsampleflags.htm
tech.root: mf
ms.assetid: 30dac293-981b-41f3-951d-186d6a603d0a
ms.date: 12/05/2018
ms.keywords: 30dac293-981b-41f3-951d-186d6a603d0a, IMFSample interface [Media Foundation],SetSampleFlags method, IMFSample.SetSampleFlags, IMFSample::SetSampleFlags, SetSampleFlags, SetSampleFlags method [Media Foundation], SetSampleFlags method [Media Foundation],IMFSample interface, mf.imfsample_setsampleflags, mfobjects/IMFSample::SetSampleFlags
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
 - IMFSample::SetSampleFlags
 - mfobjects/IMFSample::SetSampleFlags
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
 - IMFSample.SetSampleFlags
---

# IMFSample::SetSampleFlags


## -description

Sets flags associated with the sample.

Currently no flags are defined. Instead, metadata for samples is defined using attributes. To set attributes on a sample, use the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface, which <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a> inherits. For a list of sample attributes, see <a href="/windows/desktop/medfound/sample-attributes">Sample Attributes</a>.

## -parameters

### -param dwSampleFlags [in]

Reserved; must be zero.

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