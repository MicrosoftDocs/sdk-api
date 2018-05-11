---
UID: NF:mfidl.IMFAudioPolicy.GetDisplayName
title: IMFAudioPolicy::GetDisplayName
author: windows-driver-content
description: Retrieves the display name of the audio session. The Windows volume control displays this name.
old-location: mf\imfaudiopolicy_getdisplayname.htm
old-project: medfound
ms.assetid: 7826b4a1-5887-46a5-b312-91159596ccf5
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: 7826b4a1-5887-46a5-b312-91159596ccf5, GetDisplayName, GetDisplayName method [Media Foundation], GetDisplayName method [Media Foundation],IMFAudioPolicy interface, IMFAudioPolicy interface [Media Foundation],GetDisplayName method, IMFAudioPolicy.GetDisplayName, IMFAudioPolicy::GetDisplayName, mf.imfaudiopolicy_getdisplayname, mfidl/IMFAudioPolicy::GetDisplayName
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
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
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFAudioPolicy.GetDisplayName
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFAudioPolicy::GetDisplayName


## -description



Retrieves the display name of the audio session. The Windows volume control displays this name.




## -parameters




### -param pszName






#### - pbstrName [out]

Receives a pointer to the display name string. The caller must free the memory allocated for the string by calling <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.


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



If the application does not set a display name, Windows creates one.




## -see-also




<a href="https://msdn.microsoft.com/fcd4dbfb-3f9f-4089-b9cc-7b41b2c2678a">IMFAudioPolicy</a>



<a href="https://msdn.microsoft.com/5884a128-597d-432b-a706-e10c894d7965">Streaming Audio Renderer</a>
 

 

