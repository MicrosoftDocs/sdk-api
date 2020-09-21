---
UID: NF:devicetopology.IPart.GetName
title: IPart::GetName (devicetopology.h)
description: The GetName method gets the friendly name of this part.
helpviewer_keywords: ["GetName","GetName method [Core Audio]","GetName method [Core Audio]","IPart interface","IPart interface [Core Audio]","GetName method","IPart.GetName","IPart::GetName","IPartGetName","coreaudio.ipart_getname","devicetopology/IPart::GetName"]
old-location: coreaudio\ipart_getname.htm
tech.root: CoreAudio
ms.assetid: a583f445-ebb2-4072-a272-6f186aef71b3
ms.date: 12/05/2018
ms.keywords: GetName, GetName method [Core Audio], GetName method [Core Audio],IPart interface, IPart interface [Core Audio],GetName method, IPart.GetName, IPart::GetName, IPartGetName, coreaudio.ipart_getname, devicetopology/IPart::GetName
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
 - IPart::GetName
 - devicetopology/IPart::GetName
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
 - IPart.GetName
---

# IPart::GetName


## -description

The <b>GetName</b> method gets the friendly name of this part.

## -parameters

### -param ppwstrName [out]

Pointer to a pointer variable into which the method writes the address of a null-terminated, wide-character string that contains the friendly name of this part. The method allocates the storage for the string. The caller is responsible for freeing the storage, when it is no longer needed, by calling the <b>CoTaskMemFree</b> function. If the <b>GetName</b> call fails,  <i>*ppwstrName</i> is <b>NULL</b>. For information about <b>CoTaskMemFree</b>, see the Windows SDK documentation.

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
</table>

## -see-also

<a href="/windows/desktop/api/devicetopology/nn-devicetopology-ipart">IPart Interface</a>