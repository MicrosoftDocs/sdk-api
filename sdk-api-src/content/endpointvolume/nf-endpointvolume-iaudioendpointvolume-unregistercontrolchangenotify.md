---
UID: NF:endpointvolume.IAudioEndpointVolume.UnregisterControlChangeNotify
title: IAudioEndpointVolume::UnregisterControlChangeNotify (endpointvolume.h)
description: The UnregisterControlChangeNotify method deletes the registration of a client's notification callback interface that the client registered in a previous call to the IAudioEndpointVolume::RegisterControlChangeNotify method.
helpviewer_keywords: ["IAudioEndpointVolume interface [Core Audio]","UnregisterControlChangeNotify method","IAudioEndpointVolume.UnregisterControlChangeNotify","IAudioEndpointVolume::UnregisterControlChangeNotify","IAudioEndpointVolumeUnregisterControlChangeNotify","UnregisterControlChangeNotify","UnregisterControlChangeNotify method [Core Audio]","UnregisterControlChangeNotify method [Core Audio]","IAudioEndpointVolume interface","coreaudio.iaudioendpointvolume_unregistercontrolchangenotify","endpointvolume/IAudioEndpointVolume::UnregisterControlChangeNotify"]
old-location: coreaudio\iaudioendpointvolume_unregistercontrolchangenotify.htm
tech.root: CoreAudio
ms.assetid: 4ae8263b-83f5-4d9f-9e48-d78fae98c7ad
ms.date: 12/05/2018
ms.keywords: IAudioEndpointVolume interface [Core Audio],UnregisterControlChangeNotify method, IAudioEndpointVolume.UnregisterControlChangeNotify, IAudioEndpointVolume::UnregisterControlChangeNotify, IAudioEndpointVolumeUnregisterControlChangeNotify, UnregisterControlChangeNotify, UnregisterControlChangeNotify method [Core Audio], UnregisterControlChangeNotify method [Core Audio],IAudioEndpointVolume interface, coreaudio.iaudioendpointvolume_unregistercontrolchangenotify, endpointvolume/IAudioEndpointVolume::UnregisterControlChangeNotify
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
 - IAudioEndpointVolume::UnregisterControlChangeNotify
 - endpointvolume/IAudioEndpointVolume::UnregisterControlChangeNotify
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
 - IAudioEndpointVolume.UnregisterControlChangeNotify
---

# IAudioEndpointVolume::UnregisterControlChangeNotify


## -description

The <b>UnregisterControlChangeNotify</b> method deletes the registration of a client's notification callback interface that the client registered in a previous call to the <a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify">IAudioEndpointVolume::RegisterControlChangeNotify</a> method.

## -parameters

### -param pNotify [in]

Pointer to the client's <a href="/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback">IAudioEndpointVolumeCallback</a> interface. The client passed this same interface pointer to the endpoint volume object in a previous call to the <a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify">IAudioEndpointVolume::RegisterControlChangeNotify</a> method. If the <b>UnregisterControlChangeNotify</b> method succeeds, it calls the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> method on the client's <b>IAudioEndpointVolumeCallback</b> interface.

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

Before the client releases its final reference to the <a href="/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback">IAudioEndpointVolumeCallback</a> interface, it should call <b>UnregisterControlChangeNotify</b> to unregister the interface. Otherwise, the application leaks the resources held by the <b>IAudioEndpointVolumeCallback</b> and <a href="/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolume">IAudioEndpointVolume</a> objects. Note that the <a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify">IAudioEndpointVolume::RegisterControlChangeNotify</a> method calls the client's <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">IAudioEndpointVolumeCallback::AddRef</a> method, and <b>UnregisterControlChangeNotify</b> calls the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IAudioEndpointVolumeCallback::Release</a> method. If the client errs by releasing its reference to the <b>IAudioEndpointVolumeCallback</b> interface before calling <b>UnregisterControlChangeNotify</b>, the <b>IAudioEndpointVolume</b> object never releases its reference to the <b>IAudioEndpointVolumeCallback</b> interface. For example, a poorly designed <b>IAudioEndpointVolumeCallback</b> implementation might call <b>UnregisterControlChangeNotify</b> from the destructor for the <b>IAudioEndpointVolumeCallback</b> object. In this case, the client will not call <b>UnregisterControlChangeNotify</b> until the <b>IAudioEndpointVolume</b> object releases its reference to the <b>IAudioEndpointVolumeCallback</b> interface, and the <b>IAudioEndpointVolume</b> object will not release its reference to the <b>IAudioEndpointVolumeCallback</b> interface until the client calls <b>UnregisterControlChangeNotify</b>. For more information about the <b>AddRef</b> and <b>Release</b> methods, see the discussion of the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface in the Windows SDK documentation.

For a code example that calls <b>UnregisterControlChangeNotify</b>, see <a href="/windows/desktop/CoreAudio/endpoint-volume-controls">Endpoint Volume Controls</a>.

## -see-also

<a href="/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolume">IAudioEndpointVolume Interface</a>



<a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify">IAudioEndpointVolume::RegisterControlChangeNotify</a>



<a href="/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback">IAudioEndpointVolumeCallback Interface</a>