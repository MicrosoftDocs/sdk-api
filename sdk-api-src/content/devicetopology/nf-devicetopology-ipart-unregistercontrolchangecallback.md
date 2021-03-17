---
UID: NF:devicetopology.IPart.UnregisterControlChangeCallback
title: IPart::UnregisterControlChangeCallback (devicetopology.h)
description: The UnregisterControlChangeCallback method removes the registration of an IControlChangeNotify interface that the client previously registered by a call to the IPart::RegisterControlChangeCallback method.
helpviewer_keywords: ["IPart interface [Core Audio]","UnregisterControlChangeCallback method","IPart.UnregisterControlChangeCallback","IPart::UnregisterControlChangeCallback","IPartUnregisterControlChangeCallback","UnregisterControlChangeCallback","UnregisterControlChangeCallback method [Core Audio]","UnregisterControlChangeCallback method [Core Audio]","IPart interface","coreaudio.ipart_unregistercontrolchangecallback","devicetopology/IPart::UnregisterControlChangeCallback"]
old-location: coreaudio\ipart_unregistercontrolchangecallback.htm
tech.root: CoreAudio
ms.assetid: d3341421-6dab-43f3-87a8-83ee8a986a04
ms.date: 12/05/2018
ms.keywords: IPart interface [Core Audio],UnregisterControlChangeCallback method, IPart.UnregisterControlChangeCallback, IPart::UnregisterControlChangeCallback, IPartUnregisterControlChangeCallback, UnregisterControlChangeCallback, UnregisterControlChangeCallback method [Core Audio], UnregisterControlChangeCallback method [Core Audio],IPart interface, coreaudio.ipart_unregistercontrolchangecallback, devicetopology/IPart::UnregisterControlChangeCallback
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
 - IPart::UnregisterControlChangeCallback
 - devicetopology/IPart::UnregisterControlChangeCallback
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
 - IPart.UnregisterControlChangeCallback
---

# IPart::UnregisterControlChangeCallback


## -description

The <b>UnregisterControlChangeCallback</b> method removes the registration of an <a href="/windows/desktop/api/devicetopology/nn-devicetopology-icontrolchangenotify">IControlChangeNotify</a> interface that the client previously registered by a call to the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-registercontrolchangecallback">IPart::RegisterControlChangeCallback</a> method.

## -parameters

### -param pNotify [in]

Pointer to the <b>IControlChangeNotify</b> interface whose registration is to be deleted. The client passed this same interface pointer to the part object in a previous call to the <b>IPart::RegisterControlChangeCallback</b> method. If the <b>UnregisterControlChangeCallback</b> method succeeds, it calls the <b>Release</b> method on the client's <b>IControlChangeNotify</b> interface.

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
Pointer <i>pNotify</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
Interface instance  <i>*pNotify</i> is not currently registered.

</td>
</tr>
</table>

## -remarks

Before the client releases its final reference to the <b>IControlChangeNotify</b> interface, it should call <b>UnregisterControlChangeCallback</b> to unregister the interface. Otherwise, the application leaks the resources held by the <b>IControlChangeNotify</b> and <b>IPart</b> objects. Note that the <b>IPart::RegisterControlChangeCallback</b> method calls the client's <b>IControlChangeNotify::AddRef</b> method, and <b>UnregisterControlChangeCallback</b> calls the <b>IControlChangeNotify::Release</b> method. If the client errs by releasing its reference to the <b>IControlChangeNotify</b> interface before calling <b>UnregisterControlChangeCallback</b>, the <b>IPart</b> object never releases its reference to the <b>IControlChangeNotify</b> interface. For example, a poorly designed <b>IControlChangeNotify</b> implementation might call <b>UnregisterControlChangeCallback</b> from the destructor for the <b>IControlChangeNotify</b> object. In this case, the client will not call <b>UnregisterControlChangeCallback</b> until the <b>IPart</b> object releases its reference to the <b>IControlChangeNotify</b> interface, and the <b>IPart</b> object will not release its reference to the <b>IControlChangeNotify</b> interface until the client calls <b>UnregisterControlChangeCallback</b>. For more information about the <b>AddRef</b> and <b>Release</b> methods, see the discussion of the <b>IUnknown</b> interface in the Windows SDK documentation.

## -see-also

<a href="/windows/desktop/api/devicetopology/nn-devicetopology-icontrolchangenotify">IControlChangeNotify Interface</a>



<a href="/windows/desktop/api/devicetopology/nn-devicetopology-ipart">IPart Interface</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-registercontrolchangecallback">IPart::RegisterControlChangeCallback</a>