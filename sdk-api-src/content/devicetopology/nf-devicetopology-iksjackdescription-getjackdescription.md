---
UID: NF:devicetopology.IKsJackDescription.GetJackDescription
title: IKsJackDescription::GetJackDescription (devicetopology.h)
description: The GetJackDescription method gets a description of an audio jack.
old-location: coreaudio\iksjackdescription_getjackdescription.htm
tech.root: CoreAudio
ms.assetid: 84278805-3b6d-4fae-8770-f9932b0e0fab
ms.date: 12/05/2018
ms.keywords: GetJackDescription, GetJackDescription method [Core Audio], GetJackDescription method [Core Audio],IKsJackDescription interface, IKsJackDescription interface [Core Audio],GetJackDescription method, IKsJackDescription.GetJackDescription, IKsJackDescription::GetJackDescription, IKsJackDescriptionGetJackDescription, coreaudio.iksjackdescription_getjackdescription, devicetopology/IKsJackDescription::GetJackDescription
req.header: devicetopology.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKsJackDescription::GetJackDescription
 - devicetopology/IKsJackDescription::GetJackDescription
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
 - IKsJackDescription.GetJackDescription
---

# IKsJackDescription::GetJackDescription


## -description

The <b>GetJackDescription</b> method gets a description of an audio jack.

## -parameters

### -param nJack [in]

The jack index. If the connection consists of <i>n</i> jacks, the jacks are numbered from 0 to <i>n</i>– 1. To get the number of jacks, call the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-iksjackdescription-getjackcount">IKsJackDescription::GetJackCount</a> method.

### -param pDescription [out]

Pointer to a caller-allocated buffer into which the method writes a structure of type <a href="/windows/win32/api/devicetopology/ns-devicetopology-ksjack_description">KSJACK_DESCRIPTION</a> that contains information about the jack. The buffer size must be at least sizeof(KSJACK_DESCRIPTION).

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

## -remarks

When a user needs to plug an audio endpoint device into a jack or unplug it from a jack, an audio application can use the descriptive information that it retrieves from this method to help the user to find the jack. This information includes:

<ul>
<li>The physical location of the jack on the computer chassis or external box.</li>
<li>The color of the jack.</li>
<li>The type of physical connector used for the jack.</li>
<li>The mapping of channels to the jack.</li>
</ul>
For more information, see <a href="/windows/win32/api/devicetopology/ns-devicetopology-ksjack_description">KSJACK_DESCRIPTION</a>.

## -see-also

<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iksjackdescription">IKsJackDescription Interface</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-iksjackdescription-getjackcount">IKsJackDescription::GetJackCount</a>



<a href="/windows/win32/api/devicetopology/ns-devicetopology-ksjack_description">KSJACK_DESCRIPTION</a>