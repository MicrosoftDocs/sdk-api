---
UID: NF:wmcontainer.IMFASFProfile.GetStreamByNumber
title: IMFASFProfile::GetStreamByNumber (wmcontainer.h)
description: Retrieves an Advanced Systems Format (ASF) stream configuration object for a stream in the profile. This method references the stream by stream number instead of stream index.
helpviewer_keywords: ["1e3fadf0-1549-4d51-b263-727b15c55023","GetStreamByNumber","GetStreamByNumber method [Media Foundation]","GetStreamByNumber method [Media Foundation]","IMFASFProfile interface","IMFASFProfile interface [Media Foundation]","GetStreamByNumber method","IMFASFProfile.GetStreamByNumber","IMFASFProfile::GetStreamByNumber","mf.imfasfprofile_getstreambynumber","wmcontainer/IMFASFProfile::GetStreamByNumber"]
old-location: mf\imfasfprofile_getstreambynumber.htm
tech.root: mf
ms.assetid: 1e3fadf0-1549-4d51-b263-727b15c55023
ms.date: 12/05/2018
ms.keywords: 1e3fadf0-1549-4d51-b263-727b15c55023, GetStreamByNumber, GetStreamByNumber method [Media Foundation], GetStreamByNumber method [Media Foundation],IMFASFProfile interface, IMFASFProfile interface [Media Foundation],GetStreamByNumber method, IMFASFProfile.GetStreamByNumber, IMFASFProfile::GetStreamByNumber, mf.imfasfprofile_getstreambynumber, wmcontainer/IMFASFProfile::GetStreamByNumber
req.header: wmcontainer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IMFASFProfile::GetStreamByNumber
 - wmcontainer/IMFASFProfile::GetStreamByNumber
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
 - IMFASFProfile.GetStreamByNumber
---

# IMFASFProfile::GetStreamByNumber


## -description

Retrieves an Advanced Systems Format (ASF) stream configuration object for a stream in the profile. This method references the stream by stream number instead of stream index.

## -parameters

### -param wStreamNumber [in]

The stream number for which to obtain the interface pointer.

### -param ppIStream [out]

Receives a pointer to the <a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig">IMFASFStreamConfig</a> interface of the ASF stream configuration object. The caller must release the interface.

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

This method does not create a copy of the stream configuration object. The pointer that is retrieved points to the object within the profile object. You must not make any changes to the stream configuration object using this pointer, because doing so can affect the profile object in unexpected ways.

To change the configuration of the stream configuration object in the profile, you must first clone the stream configuration object by calling <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-clone">IMFASFStreamConfig::Clone</a>. Make whatever changes are required to the clone of the object and then add the updated object by calling the <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream">IMFASFProfile::SetStream</a> method.

## -see-also

<a href="/windows/desktop/medfound/asf-profile">ASF Profile</a>



<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile">IMFASFProfile</a>



<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream">IMFASFProfile::GetStream</a>



<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream">IMFASFProfile::SetStream</a>



<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig">IMFASFStreamConfig</a>