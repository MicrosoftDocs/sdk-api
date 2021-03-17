---
UID: NF:devicetopology.IPart.GetControlInterface
title: IPart::GetControlInterface (devicetopology.h)
description: The GetControlInterface method gets a reference to the specified control interface, if this part supports it.
helpviewer_keywords: ["GetControlInterface","GetControlInterface method [Core Audio]","GetControlInterface method [Core Audio]","IPart interface","IPart interface [Core Audio]","GetControlInterface method","IPart.GetControlInterface","IPart::GetControlInterface","IPartGetControlInterface","coreaudio.ipart_getcontrolinterface","devicetopology/IPart::GetControlInterface"]
old-location: coreaudio\ipart_getcontrolinterface.htm
tech.root: CoreAudio
ms.assetid: 802f3c19-5a71-41b0-922a-f216fd60495c
ms.date: 12/05/2018
ms.keywords: GetControlInterface, GetControlInterface method [Core Audio], GetControlInterface method [Core Audio],IPart interface, IPart interface [Core Audio],GetControlInterface method, IPart.GetControlInterface, IPart::GetControlInterface, IPartGetControlInterface, coreaudio.ipart_getcontrolinterface, devicetopology/IPart::GetControlInterface
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
 - IPart::GetControlInterface
 - devicetopology/IPart::GetControlInterface
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
 - IPart.GetControlInterface
---

# IPart::GetControlInterface


## -description

The <b>GetControlInterface</b> method gets a reference to the specified control interface, if this part supports it.

## -parameters

### -param nIndex [in]

The control interface number. If a part supports <i>n</i> control interfaces, the control interfaces are numbered from 0 to <i>n</i>– 1.

### -param ppInterfaceDesc [out]

Pointer to a pointer variable into which the method writes the address of the <a href="/windows/desktop/api/devicetopology/nn-devicetopology-icontrolinterface">IControlInterface</a> interface of the specified audio function. Through this method, the caller obtains a counted reference to the interface. The caller is responsible for releasing the interface, when it is no longer needed, by calling the interface's <b>Release</b> method. If the <b>GetControlInterface</b> call fails,  <i>*ppFunction</i> is <b>NULL</b>.

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
Pointer <i>ppFunction</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>nIndex</i> is out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The part does not have a control interface.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/devicetopology/nn-devicetopology-icontrolinterface">IControlInterface Interface</a>



<a href="/windows/desktop/api/devicetopology/nn-devicetopology-ipart">IPart Interface</a>