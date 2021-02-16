---
UID: NF:devicetopology.IKsFormatSupport.GetDevicePreferredFormat
title: IKsFormatSupport::GetDevicePreferredFormat (devicetopology.h)
description: The GetDevicePreferredFormat method gets the preferred audio stream format for the connection.
helpviewer_keywords: ["GetDevicePreferredFormat","GetDevicePreferredFormat method [Core Audio]","GetDevicePreferredFormat method [Core Audio]","IKsFormatSupport interface","IKsFormatSupport interface [Core Audio]","GetDevicePreferredFormat method","IKsFormatSupport.GetDevicePreferredFormat","IKsFormatSupport::GetDevicePreferredFormat","IKsFormatSupportGetDevicePreferredFormat","coreaudio.iksformatsupport_getdevicepreferredformat","devicetopology/IKsFormatSupport::GetDevicePreferredFormat"]
old-location: coreaudio\iksformatsupport_getdevicepreferredformat.htm
tech.root: CoreAudio
ms.assetid: a550ed25-020f-4d09-bfb4-76680539c50a
ms.date: 12/05/2018
ms.keywords: GetDevicePreferredFormat, GetDevicePreferredFormat method [Core Audio], GetDevicePreferredFormat method [Core Audio],IKsFormatSupport interface, IKsFormatSupport interface [Core Audio],GetDevicePreferredFormat method, IKsFormatSupport.GetDevicePreferredFormat, IKsFormatSupport::GetDevicePreferredFormat, IKsFormatSupportGetDevicePreferredFormat, coreaudio.iksformatsupport_getdevicepreferredformat, devicetopology/IKsFormatSupport::GetDevicePreferredFormat
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
 - IKsFormatSupport::GetDevicePreferredFormat
 - devicetopology/IKsFormatSupport::GetDevicePreferredFormat
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
 - IKsFormatSupport.GetDevicePreferredFormat
---

# IKsFormatSupport::GetDevicePreferredFormat


## -description

The <b>GetDevicePreferredFormat</b> method gets the preferred audio stream format for the connection.

## -parameters

### -param ppKsFormat [out]

Pointer to a pointer variable into which the method writes the address of a buffer that contains the format specifier for the preferred format. The specifier begins with a <b>KSDATAFORMAT</b> structure that might be followed by additional format information. The method allocates the storage for the format specifier. The caller is responsible for freeing the storage, when it is no longer needed, by calling the <b>CoTaskMemFree</b> function. If the method fails,  <i>*ppKsFormat</i> is <b>NULL</b>. For more information about <b>KSDATAFORMAT</b>, format specifiers, and <b>CoTaskMemFree</b>, see the Windows DDK documentation.

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
Pointer <i>ppKsFormat</i> is <b>NULL</b>.

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

## -see-also

<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iksformatsupport">IKsFormatSupport Interface</a>