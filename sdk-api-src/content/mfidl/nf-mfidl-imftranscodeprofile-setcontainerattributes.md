---
UID: NF:mfidl.IMFTranscodeProfile.SetContainerAttributes
title: IMFTranscodeProfile::SetContainerAttributes (mfidl.h)
description: Sets container configuration settings in the transcode profile.
helpviewer_keywords: ["IMFTranscodeProfile interface [Media Foundation]","SetContainerAttributes method","IMFTranscodeProfile.SetContainerAttributes","IMFTranscodeProfile::SetContainerAttributes","SetContainerAttributes","SetContainerAttributes method [Media Foundation]","SetContainerAttributes method [Media Foundation]","IMFTranscodeProfile interface","mf.imftranscodeprofile_setcontainerattributes","mfidl/IMFTranscodeProfile::SetContainerAttributes"]
old-location: mf\imftranscodeprofile_setcontainerattributes.htm
tech.root: mf
ms.assetid: c62021cf-85f1-4a85-9263-b7883464f5f8
ms.date: 12/05/2018
ms.keywords: IMFTranscodeProfile interface [Media Foundation],SetContainerAttributes method, IMFTranscodeProfile.SetContainerAttributes, IMFTranscodeProfile::SetContainerAttributes, SetContainerAttributes, SetContainerAttributes method [Media Foundation], SetContainerAttributes method [Media Foundation],IMFTranscodeProfile interface, mf.imftranscodeprofile_setcontainerattributes, mfidl/IMFTranscodeProfile::SetContainerAttributes
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IMFTranscodeProfile::SetContainerAttributes
 - mfidl/IMFTranscodeProfile::SetContainerAttributes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFTranscodeProfile.SetContainerAttributes
---

# IMFTranscodeProfile::SetContainerAttributes


## -description

Sets container configuration settings  in the transcode profile.

 For example code, see <a href="/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile">MFCreateTranscodeProfile</a>.

## -parameters

### -param pAttrs [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface of an attribute store that contains the configuration settings for the container in which the transcoded file will be stored. The specified attribute values overwrite any existing values stored in the transcode profile. 

The following list shows the container attributes that can be set:

<ul>
<li>
<a href="/windows/desktop/medfound/mf-transcode-adjust-profile">MF_TRANSCODE_ADJUST_PROFILE</a>
</li>
<li>
<a href="/windows/desktop/medfound/mf-transcode-containertype">MF_TRANSCODE_CONTAINERTYPE</a>
</li>
<li>
<a href="/windows/desktop/medfound/mf-transcode-skip-metadata-transfer">MF_TRANSCODE_SKIP_METADATA_TRANSFER</a>
</li>
<li>
<a href="/windows/desktop/medfound/mf-transcode-topologymode">MF_TRANSCODE_TOPOLOGYMODE</a>
</li>
<li>
<a href="/windows/desktop/medfound/mft-fieldofuse-unlock-attribute">MFT_FIELDOFUSE_UNLOCK</a>
</li>
</ul>
To create the attribute store, call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes">MFCreateAttributes</a>. To set a specific attribute value in the attribute store, the caller must call the appropriate <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> methods depending on the data type of the attribute.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/medfound/attributes-and-properties">Attributes in Media Foundation</a>



<a href="/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile">IMFTranscodeProfile</a>



<a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes">MFCreateAttributes</a>



<a href="/windows/desktop/medfound/transcode-api">Transcode API</a>