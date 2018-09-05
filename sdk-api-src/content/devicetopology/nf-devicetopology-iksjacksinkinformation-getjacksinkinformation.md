---
UID: NF:devicetopology.IKsJackSinkInformation.GetJackSinkInformation
title: IKsJackSinkInformation::GetJackSinkInformation
author: windows-sdk-content
description: The GetJackSinkInformation method retrieves the sink information for the specified jack.
old-location: coreaudio\iksjacksinkinformation_getjacksinkinformation.htm
old-project: CoreAudio
ms.assetid: ca4165ce-433a-4a8f-9853-bbe812de90ca
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: GetJackSinkInformation, GetJackSinkInformation method [Core Audio], GetJackSinkInformation method [Core Audio],IKsJackSinkInformation interface, IKsJackSinkInformation interface [Core Audio],GetJackSinkInformation method, IKsJackSinkInformation.GetJackSinkInformation, IKsJackSinkInformation::GetJackSinkInformation, coreaudio.iksjacksinkinformation_getjacksinkinformation, devicetopology/IKsJackSinkInformation::GetJackSinkInformation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: devicetopology.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: ConnectorType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Devicetopology.h
api_name:
 - IKsJackSinkInformation.GetJackSinkInformation
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IKsJackSinkInformation::GetJackSinkInformation


## -description


The <b>GetJackSinkInformation</b> method retrieves the sink information for the specified jack.


## -parameters




### -param pJackSinkInformation [out]

Pointer to a caller-allocated buffer that receives the sink information of the jack in a <a href="https://msdn.microsoft.com/ee7211d8-a34f-40c9-9925-7bb40792bae9">KSJACK_SINK_INFORMATION</a> structure. The buffer size must be at least <code>sizeof(KSJACK_SINK_INFORMATION)</code>.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>nJack</i> is not a valid jack index.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer <i>pDescription</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/4116a912-5ff2-4fc0-96c6-61d1e62cd973">IKsJackSinkInformation</a>
 

 

