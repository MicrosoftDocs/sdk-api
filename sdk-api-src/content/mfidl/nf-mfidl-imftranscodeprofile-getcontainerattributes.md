---
UID: NF:mfidl.IMFTranscodeProfile.GetContainerAttributes
title: IMFTranscodeProfile::GetContainerAttributes
author: windows-sdk-content
description: Gets the container settings that are currently set in the transcode profile.
old-location: mf\imftranscodeprofile_getcontainerattributes.htm
tech.root: medfound
ms.assetid: 29bf5834-78af-4521-95b1-dfd5764e96fc
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetContainerAttributes, GetContainerAttributes method [Media Foundation], GetContainerAttributes method [Media Foundation],IMFTranscodeProfile interface, IMFTranscodeProfile interface [Media Foundation],GetContainerAttributes method, IMFTranscodeProfile.GetContainerAttributes, IMFTranscodeProfile::GetContainerAttributes, mf.imftranscodeprofile_getcontainerattributes, mfidl/IMFTranscodeProfile::GetContainerAttributes
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IMFTranscodeProfile.GetContainerAttributes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFTranscodeProfile::GetContainerAttributes


## -description


Gets the container settings that are currently set in the transcode profile.


## -parameters




### -param ppAttrs [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface of the attribute store containing the current container type for the output file. Caller must release the interface pointer.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If there are no container attributes set in the transcode profile, the call to <b>GetContainerAttributes</b>  succeeds and  <i>ppAttrs</i> receives <b>NULL</b>.

 To get a specific attribute value, the caller must call the appropriate <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> method depending on the data type of the attribute. The following list shows the container attributes:

<ul>
<li>
<a href="https://msdn.microsoft.com/97fd968a-6843-4695-aece-02f9acd618fd">MF_TRANSCODE_CONTAINERTYPE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0fbfc035-c9d1-4014-a28a-93d7e6adc718">MF_TRANSCODE_SKIP_METADATA_TRANSFER</a>
</li>
<li>
<a href="https://msdn.microsoft.com/33db8621-114a-4531-908f-f30034441973">MF_TRANSCODE_TOPOLOGYMODE</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/44af5e03-5f0a-4564-b9d6-b8c935df35b2">Attributes in Media Foundation</a>



<a href="https://msdn.microsoft.com/82e012e0-84d8-4791-8b6f-bda58b498a90">IMFTranscodeProfile</a>



<a href="https://msdn.microsoft.com/24bf68a8-39bf-4302-b28c-71bb23b63469">Transcode API</a>
 

 

