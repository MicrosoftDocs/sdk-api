---
UID: NF:mfidl.IMFAudioPolicy.SetDisplayName
title: IMFAudioPolicy::SetDisplayName
author: windows-sdk-content
description: Sets the display name of the audio session. The Windows volume control displays this name.
old-location: mf\imfaudiopolicy_setdisplayname.htm
old-project: medfound
ms.assetid: 4cd48400-8d12-4a6b-95fd-bf6ae7700cb8
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: 4cd48400-8d12-4a6b-95fd-bf6ae7700cb8, IMFAudioPolicy interface [Media Foundation],SetDisplayName method, IMFAudioPolicy.SetDisplayName, IMFAudioPolicy::SetDisplayName, SetDisplayName, SetDisplayName method [Media Foundation], SetDisplayName method [Media Foundation],IMFAudioPolicy interface, mf.imfaudiopolicy_setdisplayname, mfidl/IMFAudioPolicy::SetDisplayName
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: MFSensorDeviceMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFAudioPolicy.SetDisplayName
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFAudioPolicy::SetDisplayName


## -description



Sets the display name of the audio session. The Windows volume control displays this name.




## -parameters




### -param pszName [in]

A null-terminated wide-character string that contains the display name.


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
 

 

