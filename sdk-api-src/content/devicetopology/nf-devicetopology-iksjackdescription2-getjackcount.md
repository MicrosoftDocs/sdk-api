---
UID: NF:devicetopology.IKsJackDescription2.GetJackCount
title: IKsJackDescription2::GetJackCount (devicetopology.h)
description: The GetJackCount method gets the number of jacks on the connector, which are required to connect to an endpoint device.
helpviewer_keywords: ["GetJackCount","GetJackCount method [Core Audio]","GetJackCount method [Core Audio]","IKsJackDescription2 interface","IKsJackDescription2 interface [Core Audio]","GetJackCount method","IKsJackDescription2.GetJackCount","IKsJackDescription2::GetJackCount","coreaudio.iksjackdescription2_getjackcount","devicetopology/IKsJackDescription2::GetJackCount"]
old-location: coreaudio\iksjackdescription2_getjackcount.htm
tech.root: CoreAudio
ms.assetid: b7ebe746-4680-4921-a1fd-1940e306f4eb
ms.date: 12/05/2018
ms.keywords: GetJackCount, GetJackCount method [Core Audio], GetJackCount method [Core Audio],IKsJackDescription2 interface, IKsJackDescription2 interface [Core Audio],GetJackCount method, IKsJackDescription2.GetJackCount, IKsJackDescription2::GetJackCount, coreaudio.iksjackdescription2_getjackcount, devicetopology/IKsJackDescription2::GetJackCount
req.header: devicetopology.h
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
 - IKsJackDescription2::GetJackCount
 - devicetopology/IKsJackDescription2::GetJackCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Devicetopology.h
api_name:
 - IKsJackDescription2.GetJackCount
---

# IKsJackDescription2::GetJackCount


## -description

The <b>GetJackCount</b> method gets the number of jacks on the connector, which are required to connect to an endpoint device.

## -parameters

### -param pcJacks [out]

Receives the number of audio jacks associated with the connector.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer <i>pcJacks</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iksjackdescription2">IKsJackDescription2</a>