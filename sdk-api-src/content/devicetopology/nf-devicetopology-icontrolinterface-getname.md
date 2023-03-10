---
UID: NF:devicetopology.IControlInterface.GetName
title: IControlInterface::GetName (devicetopology.h)
description: The GetName method gets the friendly name for the audio function that the control interface encapsulates.
helpviewer_keywords: ["GetName","GetName method [Core Audio]","GetName method [Core Audio]","IControlInterface interface","IControlInterface interface [Core Audio]","GetName method","IControlInterface.GetName","IControlInterface::GetName","IControlInterfaceGetName","coreaudio.icontrolinterface_getname","devicetopology/IControlInterface::GetName"]
old-location: coreaudio\icontrolinterface_getname.htm
tech.root: CoreAudio
ms.assetid: 591e96ba-aaf1-42ba-9526-f839c30947d3
ms.date: 12/05/2018
ms.keywords: GetName, GetName method [Core Audio], GetName method [Core Audio],IControlInterface interface, IControlInterface interface [Core Audio],GetName method, IControlInterface.GetName, IControlInterface::GetName, IControlInterfaceGetName, coreaudio.icontrolinterface_getname, devicetopology/IControlInterface::GetName
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
 - IControlInterface::GetName
 - devicetopology/IControlInterface::GetName
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
 - IControlInterface.GetName
---

# IControlInterface::GetName


## -description

The <b>GetName</b> method gets the friendly name for the audio function that the control interface encapsulates.

## -parameters

### -param ppwstrName [out]

Pointer to a string pointer into which the method writes the address of a null-terminated, wide-character string that contains the friendly name. The method allocates the storage for the string. The caller is responsible for freeing the storage, when it is no longer needed, by calling the <b>CoTaskMemFree</b> function. If the <b>GetName</b> call fails,  <i>*ppwstrName</i> is <b>NULL</b>. For information about <b>CoTaskMemFree</b>, see the Windows SDK documentation.

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
Pointer <i>ppwstrName</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

</td>
</tr>
</table>

## -remarks

As an example of a friendly name, a subunit with an <a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudiopeakmeter">IAudioPeakMeter</a> interface might have the friendly name "peak meter".

## -see-also

<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudiopeakmeter">IAudioPeakMeter Interface</a>



<a href="/windows/desktop/api/devicetopology/nn-devicetopology-icontrolinterface">IControlInterface Interface</a>