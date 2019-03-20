---
UID: NF:mfidl.IMFTranscodeProfile.SetContainerAttributes
title: IMFTranscodeProfile::SetContainerAttributes (mfidl.h)
author: windows-sdk-content
description: Sets container configuration settings in the transcode profile.
old-location: mf\imftranscodeprofile_setcontainerattributes.htm
tech.root: medfound
ms.assetid: c62021cf-85f1-4a85-9263-b7883464f5f8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMFTranscodeProfile interface [Media Foundation],SetContainerAttributes method, IMFTranscodeProfile.SetContainerAttributes, IMFTranscodeProfile::SetContainerAttributes, SetContainerAttributes, SetContainerAttributes method [Media Foundation], SetContainerAttributes method [Media Foundation],IMFTranscodeProfile interface, mf.imftranscodeprofile_setcontainerattributes, mfidl/IMFTranscodeProfile::SetContainerAttributes
ms.topic: method
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
 - IMFTranscodeProfile.SetContainerAttributes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFTranscodeProfile::SetContainerAttributes


## -description


Sets container configuration settings  in the transcode profile.

 For example code, see <a href="https://msdn.microsoft.com/2a482c6f-6e20-419a-a7eb-085c41cc8186">MFCreateTranscodeProfile</a>.


## -parameters




### -param pAttrs [in]

Pointer to the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface of an attribute store that contains the configuration settings for the container in which the transcoded file will be stored. The specified attribute values overwrite any existing values stored in the transcode profile. 

The following list shows the container attributes that can be set:

<ul>
<li>
<a href="https://msdn.microsoft.com/6782e080-284b-458d-8bc0-6e131a529e7b">MF_TRANSCODE_ADJUST_PROFILE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/97fd968a-6843-4695-aece-02f9acd618fd">MF_TRANSCODE_CONTAINERTYPE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0fbfc035-c9d1-4014-a28a-93d7e6adc718">MF_TRANSCODE_SKIP_METADATA_TRANSFER</a>
</li>
<li>
<a href="https://msdn.microsoft.com/33db8621-114a-4531-908f-f30034441973">MF_TRANSCODE_TOPOLOGYMODE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7f48967e-375a-4019-b14f-2f457b616cc0">MFT_FIELDOFUSE_UNLOCK</a>
</li>
</ul>
To create the attribute store, call <a href="https://msdn.microsoft.com/a79b1edd-5ca1-4550-a6ce-58073155affd">MFCreateAttributes</a>. To set a specific attribute value in the attribute store, the caller must call the appropriate <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> methods depending on the data type of the attribute.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/44af5e03-5f0a-4564-b9d6-b8c935df35b2">Attributes in Media Foundation</a>



<a href="https://msdn.microsoft.com/82e012e0-84d8-4791-8b6f-bda58b498a90">IMFTranscodeProfile</a>



<a href="https://msdn.microsoft.com/a79b1edd-5ca1-4550-a6ce-58073155affd">MFCreateAttributes</a>



<a href="https://msdn.microsoft.com/24bf68a8-39bf-4302-b28c-71bb23b63469">Transcode API</a>
 

 

