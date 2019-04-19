---
UID: NF:endpointvolume.IAudioEndpointVolume.RegisterControlChangeNotify
title: IAudioEndpointVolume::RegisterControlChangeNotify (endpointvolume.h)
author: windows-sdk-content
description: The RegisterControlChangeNotify method registers a client's notification callback interface.
old-location: coreaudio\iaudioendpointvolume_registercontrolchangenotify.htm
tech.root: CoreAudio
ms.assetid: 0a5711fa-700a-44ae-beed-aec421365b4c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAudioEndpointVolume interface [Core Audio],RegisterControlChangeNotify method, IAudioEndpointVolume.RegisterControlChangeNotify, IAudioEndpointVolume::RegisterControlChangeNotify, IAudioEndpointVolumeRegisterControlChangeNotify, RegisterControlChangeNotify, RegisterControlChangeNotify method [Core Audio], RegisterControlChangeNotify method [Core Audio],IAudioEndpointVolume interface, coreaudio.iaudioendpointvolume_registercontrolchangenotify, endpointvolume/IAudioEndpointVolume::RegisterControlChangeNotify
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Endpointvolume.h
api_name:
 - IAudioEndpointVolume.RegisterControlChangeNotify
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAudioEndpointVolume::RegisterControlChangeNotify


## -description



The <b>RegisterControlChangeNotify</b> method registers a client's notification callback interface.




## -parameters




### -param pNotify [in]

Pointer to the <a href="https://msdn.microsoft.com/0b631d1b-f89c-4789-a09c-875b24a48a89">IAudioEndpointVolumeCallback</a> interface that the client is registering for notification callbacks. If the <b>RegisterControlChangeNotify</b> method succeeds, it calls the <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a> method on the client's <b>IAudioEndpointVolumeCallback</b> interface.


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



This method registers an <a href="https://msdn.microsoft.com/0b631d1b-f89c-4789-a09c-875b24a48a89">IAudioEndpointVolumeCallback</a> interface to be called by the system when the volume level or muting state of an endpoint changes. The caller implements the <b>IAudioEndpointVolumeCallback</b> interface.

When notifications are no longer needed, the client can call the <a href="https://msdn.microsoft.com/4ae8263b-83f5-4d9f-9e48-d78fae98c7ad">IAudioEndpointVolume::UnregisterControlChangeNotify</a> method to terminate the notifications.

Before the client releases its final reference to the <a href="https://msdn.microsoft.com/0b631d1b-f89c-4789-a09c-875b24a48a89">IAudioEndpointVolumeCallback</a> interface, it should call <a href="https://msdn.microsoft.com/4ae8263b-83f5-4d9f-9e48-d78fae98c7ad">UnregisterControlChangeNotify</a> to unregister the interface. Otherwise, the application leaks the resources held by the <b>IAudioEndpointVolumeCallback</b> and <a href="https://msdn.microsoft.com/5e3e7ffc-8822-4b1b-b9af-206ec1e767e2">IAudioEndpointVolume</a> objects. Note that <b>RegisterControlChangeNotify</b> calls the client's <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">IAudioEndpointVolumeCallback::AddRef</a> method, and <b>UnregisterControlChangeNotify</b> calls the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IAudioEndpointVolumeCallback::Release</a> method. If the client errs by releasing its reference to the <b>IAudioEndpointVolumeCallback</b> interface before calling <b>UnregisterControlChangeNotify</b>, the <b>IAudioEndpointVolume</b> object never releases its reference to the <b>IAudioEndpointVolumeCallback</b> interface. For example, a poorly designed <b>IAudioEndpointVolumeCallback</b> implementation might call <b>UnregisterControlChangeNotify</b> from the destructor for the <b>IAudioEndpointVolumeCallback</b> object. In this case, the client will not call <b>UnregisterControlChangeNotify</b> until the <b>IAudioEndpointVolume</b> object releases its reference to the <b>IAudioEndpointVolumeCallback</b> interface, and the <b>IAudioEndpointVolume</b> object will not release its reference to the <b>IAudioEndpointVolumeCallback</b> interface until the client calls <b>UnregisterControlChangeNotify</b>. For more information about the <b>AddRef</b> and <b>Release</b> methods, see the discussion of the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface in the Windows SDK documentation.

In addition, the client should call <a href="https://msdn.microsoft.com/4ae8263b-83f5-4d9f-9e48-d78fae98c7ad">UnregisterControlChangeNotify</a> before releasing the final reference to the <a href="https://msdn.microsoft.com/5e3e7ffc-8822-4b1b-b9af-206ec1e767e2">IAudioEndpointVolume</a> object. Otherwise, the object leaks the storage that it allocated to hold the registration information. After registering a notification interface, the client continues to receive notifications for only as long as the <b>IAudioEndpointVolume</b> object exists.

For a code example that calls <b>RegisterControlChangeNotify</b>, see <a href="https://msdn.microsoft.com/667c3659-69ae-469d-9ae0-e32a189cbc71">Endpoint Volume Controls</a>.




## -see-also




<a href="https://msdn.microsoft.com/5e3e7ffc-8822-4b1b-b9af-206ec1e767e2">IAudioEndpointVolume Interface</a>



<a href="https://msdn.microsoft.com/4ae8263b-83f5-4d9f-9e48-d78fae98c7ad">IAudioEndpointVolume::UnregisterControlChangeNotify</a>



<a href="https://msdn.microsoft.com/0b631d1b-f89c-4789-a09c-875b24a48a89">IAudioEndpointVolumeCallback Interface</a>
 

 

