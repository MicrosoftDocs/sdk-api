---
UID: NF:endpointvolume.IAudioEndpointVolume.RegisterControlChangeNotify
title: IAudioEndpointVolume::RegisterControlChangeNotify (endpointvolume.h)
description: The RegisterControlChangeNotify method registers a client's notification callback interface.
helpviewer_keywords: ["IAudioEndpointVolume interface [Core Audio]","RegisterControlChangeNotify method","IAudioEndpointVolume.RegisterControlChangeNotify","IAudioEndpointVolume::RegisterControlChangeNotify","IAudioEndpointVolumeRegisterControlChangeNotify","RegisterControlChangeNotify","RegisterControlChangeNotify method [Core Audio]","RegisterControlChangeNotify method [Core Audio]","IAudioEndpointVolume interface","coreaudio.iaudioendpointvolume_registercontrolchangenotify","endpointvolume/IAudioEndpointVolume::RegisterControlChangeNotify"]
old-location: coreaudio\iaudioendpointvolume_registercontrolchangenotify.htm
tech.root: CoreAudio
ms.assetid: 0a5711fa-700a-44ae-beed-aec421365b4c
ms.date: 12/05/2018
ms.keywords: IAudioEndpointVolume interface [Core Audio],RegisterControlChangeNotify method, IAudioEndpointVolume.RegisterControlChangeNotify, IAudioEndpointVolume::RegisterControlChangeNotify, IAudioEndpointVolumeRegisterControlChangeNotify, RegisterControlChangeNotify, RegisterControlChangeNotify method [Core Audio], RegisterControlChangeNotify method [Core Audio],IAudioEndpointVolume interface, coreaudio.iaudioendpointvolume_registercontrolchangenotify, endpointvolume/IAudioEndpointVolume::RegisterControlChangeNotify
req.header: endpointvolume.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - IAudioEndpointVolume::RegisterControlChangeNotify
 - endpointvolume/IAudioEndpointVolume::RegisterControlChangeNotify
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Endpointvolume.h
api_name:
 - IAudioEndpointVolume.RegisterControlChangeNotify
---

# IAudioEndpointVolume::RegisterControlChangeNotify


## -description

The <b>RegisterControlChangeNotify</b> method registers a client's notification callback interface.

## -parameters

### -param pNotify [in]

Pointer to the <a href="/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback">IAudioEndpointVolumeCallback</a> interface that the client is registering for notification callbacks. If the <b>RegisterControlChangeNotify</b> method succeeds, it calls the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> method on the client's <b>IAudioEndpointVolumeCallback</b> interface.

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
Parameter <i>pNotify</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

This method registers an <a href="/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback">IAudioEndpointVolumeCallback</a> interface to be called by the system when the volume level or muting state of an endpoint changes. The caller implements the <b>IAudioEndpointVolumeCallback</b> interface.

When notifications are no longer needed, the client can call the <a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify">IAudioEndpointVolume::UnregisterControlChangeNotify</a> method to terminate the notifications.

Before the client releases its final reference to the <a href="/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback">IAudioEndpointVolumeCallback</a> interface, it should call <a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify">UnregisterControlChangeNotify</a> to unregister the interface. Otherwise, the application leaks the resources held by the <b>IAudioEndpointVolumeCallback</b> and <a href="/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolume">IAudioEndpointVolume</a> objects. Note that <b>RegisterControlChangeNotify</b> calls the client's <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">IAudioEndpointVolumeCallback::AddRef</a> method, and <b>UnregisterControlChangeNotify</b> calls the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IAudioEndpointVolumeCallback::Release</a> method. If the client errs by releasing its reference to the <b>IAudioEndpointVolumeCallback</b> interface before calling <b>UnregisterControlChangeNotify</b>, the <b>IAudioEndpointVolume</b> object never releases its reference to the <b>IAudioEndpointVolumeCallback</b> interface. For example, a poorly designed <b>IAudioEndpointVolumeCallback</b> implementation might call <b>UnregisterControlChangeNotify</b> from the destructor for the <b>IAudioEndpointVolumeCallback</b> object. In this case, the client will not call <b>UnregisterControlChangeNotify</b> until the <b>IAudioEndpointVolume</b> object releases its reference to the <b>IAudioEndpointVolumeCallback</b> interface, and the <b>IAudioEndpointVolume</b> object will not release its reference to the <b>IAudioEndpointVolumeCallback</b> interface until the client calls <b>UnregisterControlChangeNotify</b>. For more information about the <b>AddRef</b> and <b>Release</b> methods, see the discussion of the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface in the Windows SDK documentation.

In addition, the client should call <a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify">UnregisterControlChangeNotify</a> before releasing the final reference to the <a href="/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolume">IAudioEndpointVolume</a> object. Otherwise, the object leaks the storage that it allocated to hold the registration information. After registering a notification interface, the client continues to receive notifications for only as long as the <b>IAudioEndpointVolume</b> object exists.

For a code example that calls <b>RegisterControlChangeNotify</b>, see <a href="/windows/desktop/CoreAudio/endpoint-volume-controls">Endpoint Volume Controls</a>.

## -see-also

<a href="/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolume">IAudioEndpointVolume Interface</a>



<a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify">IAudioEndpointVolume::UnregisterControlChangeNotify</a>



<a href="/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback">IAudioEndpointVolumeCallback Interface</a>