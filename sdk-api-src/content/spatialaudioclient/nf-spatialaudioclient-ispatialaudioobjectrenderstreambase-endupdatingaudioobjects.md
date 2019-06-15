---
UID: NF:spatialaudioclient.ISpatialAudioObjectRenderStreamBase.EndUpdatingAudioObjects
title: ISpatialAudioObjectRenderStreamBase::EndUpdatingAudioObjects (spatialaudioclient.h)
author: windows-sdk-content
description: Notifies the system that the app has finished supplying audio data for the spatial audio objects activated with ActivateSpatialAudioObject.
old-location: coreaudio\ispatialaudioobjectrenderstream_endupdatingaudioobjects.htm
tech.root: CoreAudio
ms.assetid: 111DB695-66F6-45DD-B3B6-1DFB0D5D29FC
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EndUpdatingAudioObjects, EndUpdatingAudioObjects method [Core Audio], EndUpdatingAudioObjects method [Core Audio],ISpatialAudioObjectRenderStreamBase interface, ISpatialAudioObjectRenderStreamBase interface [Core Audio],EndUpdatingAudioObjects method, ISpatialAudioObjectRenderStreamBase.EndUpdatingAudioObjects, ISpatialAudioObjectRenderStreamBase::EndUpdatingAudioObjects, coreaudio.ispatialaudioobjectrenderstream_endupdatingaudioobjects, spatialaudioclient/ISpatialAudioObjectRenderStreamBase::EndUpdatingAudioObjects
ms.topic: method
req.header: spatialaudioclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - spatialaudioclient.h
api_name:
 - ISpatialAudioObjectRenderStreamBase.EndUpdatingAudioObjects
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISpatialAudioObjectRenderStreamBase::EndUpdatingAudioObjects


## -description


Notifies the system that the app has finished supplying audio data for the spatial audio objects activated with <a href="https://docs.microsoft.com/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject">ActivateSpatialAudioObject</a>.


## -parameters






## -returns



If the method succeeds, it returns S_OK. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SPTLAUDCLNT_E_OUT_OF_ORDER</b></dt>
</dl>
</td>
<td width="60%">
<b>EndUpdatingAudioObjects</b> was called before <a href="https://docs.microsoft.com/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects">BeginUpdatingAudioObjects</a>.

</td>
</tr>
</table>
 




## -remarks



The pointers retrieved with <a href="https://docs.microsoft.com/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-getbuffer">ISpatialAudioObjectBase::GetBuffer</a> can no longer be used after this method is called.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream">ISpatialAudioObjectRenderStream</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt829728(v=VS.85).aspx">ISpatialAudioObjectRenderStreamBase</a>
 

 

