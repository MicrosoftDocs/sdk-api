---
UID: NF:devicetopology.IKsJackDescription2.GetJackDescription2
title: IKsJackDescription2::GetJackDescription2 (devicetopology.h)
description: The GetJackDescription2 method gets the description of a specified audio jack.
old-location: coreaudio\iksjackdescription2_getjackdescription2.htm
tech.root: CoreAudio
ms.assetid: 724a75c2-22be-431c-b29a-8bf916d085e7
ms.date: 12/05/2018
ms.keywords: GetJackDescription2, GetJackDescription2 method [Core Audio], GetJackDescription2 method [Core Audio],IKsJackDescription2 interface, IKsJackDescription2 interface [Core Audio],GetJackDescription2 method, IKsJackDescription2.GetJackDescription2, IKsJackDescription2::GetJackDescription2, coreaudio.iksjackdescription2_getjackdescription2, devicetopology/IKsJackDescription2::GetJackDescription2
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
 - IKsJackDescription2::GetJackDescription2
 - devicetopology/IKsJackDescription2::GetJackDescription2
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
 - IKsJackDescription2.GetJackDescription2
---

# IKsJackDescription2::GetJackDescription2


## -description

The <b>GetJackDescription2</b> method gets the description of a specified audio jack.

## -parameters

### -param nJack [in]

The index of the jack to get a description for. If the connection consists of <i>n</i> jacks, the jacks are numbered from 0 to <i>n</i>– 1. To get the number of jacks, call the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-iksjackdescription2-getjackcount">IKsJackDescription::GetJackCount</a> method.

### -param pDescription2 [out]

Pointer to a caller-allocated buffer into which the method writes a structure of type <a href="/windows/win32/api/devicetopology/ns-devicetopology-ksjack_description2">KSJACK_DESCRIPTION2</a> that contains information about the jack. The buffer size must be at least <code>sizeof(KSJACK_DESCRIPTION2)</code>.

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

<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iksjackdescription2">IKsJackDescription2</a>