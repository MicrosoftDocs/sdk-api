---
UID: NF:mfidl.IMFTranscodeProfile.GetContainerAttributes
title: IMFTranscodeProfile::GetContainerAttributes (mfidl.h)

description: Gets the container settings that are currently set in the transcode profile.
old-location: mf\imftranscodeprofile_getcontainerattributes.htm
tech.root: medfound
ms.assetid: 29bf5834-78af-4521-95b1-dfd5764e96fc

ms.date: 12/05/2018
ms.keywords: GetContainerAttributes, GetContainerAttributes method [Media Foundation], GetContainerAttributes method [Media Foundation],IMFTranscodeProfile interface, IMFTranscodeProfile interface [Media Foundation],GetContainerAttributes method, IMFTranscodeProfile.GetContainerAttributes, IMFTranscodeProfile::GetContainerAttributes, mf.imftranscodeprofile_getcontainerattributes, mfidl/IMFTranscodeProfile::GetContainerAttributes
ms.topic: method
f1_keywords: 
 - "mfidl/IMFTranscodeProfile.GetContainerAttributes"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFTranscodeProfile.GetContainerAttributes
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFTranscodeProfile::GetContainerAttributes


## -description


Gets the container settings that are currently set in the transcode profile.


## -parameters




### -param ppAttrs [out]

Receives a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface of the attribute store containing the current container type for the output file. Caller must release the interface pointer.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If there are no container attributes set in the transcode profile, the call to <b>GetContainerAttributes</b>  succeeds and  <i>ppAttrs</i> receives <b>NULL</b>.

 To get a specific attribute value, the caller must call the appropriate <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> method depending on the data type of the attribute. The following list shows the container attributes:

<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/medfound/mf-transcode-containertype">MF_TRANSCODE_CONTAINERTYPE</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/medfound/mf-transcode-skip-metadata-transfer">MF_TRANSCODE_SKIP_METADATA_TRANSFER</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/medfound/mf-transcode-topologymode">MF_TRANSCODE_TOPOLOGYMODE</a>
</li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/attributes-and-properties">Attributes in Media Foundation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile">IMFTranscodeProfile</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/transcode-api">Transcode API</a>
 

 

