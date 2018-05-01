---
UID: NF:d3d11_4.ID3D11Device4.RegisterDeviceRemovedEvent
title: ID3D11Device4::RegisterDeviceRemovedEvent method
author: windows-driver-content
description: Registers the &#0034;device removed&#0034; event and indicates when a Direct3D device has become removed for any reason, using an asynchronous notification mechanism.
old-location: direct3d11\id3d11device4_registerdeviceremovedevent.htm
old-project: direct3d11
ms.assetid: 6C564C67-9166-4F65-B099-3DDDECCEDC40
ms.author: windowsdriverdev
ms.date: 4/6/2018
ms.keywords: ID3D11Device4, ID3D11Device4 interface [Direct3D 11], RegisterDeviceRemovedEvent method, ID3D11Device4::RegisterDeviceRemovedEvent, RegisterDeviceRemovedEvent method [Direct3D 11], RegisterDeviceRemovedEvent method [Direct3D 11], ID3D11Device4 interface, RegisterDeviceRemovedEvent,ID3D11Device4.RegisterDeviceRemovedEvent, d3d11_4/ID3D11Device4::RegisterDeviceRemovedEvent, direct3d11.id3d11device4_registerdeviceremovedevent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11_4.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: D3D11_UNORDERED_ACCESS_VIEW_DESC1
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	d3d11.lib
-	d3d11.dll
api_name:
-	ID3D11Device4.RegisterDeviceRemovedEvent
product: Windows
targetos: Windows
req.lib: D3d11.lib
req.dll: 
req.irql: 
---

# ID3D11Device4::RegisterDeviceRemovedEvent method


## -description



          Registers the "device removed" event and indicates when a Direct3D device has become removed for any reason, using an asynchronous notification mechanism.
        


## -parameters




### -param hEvent [in]

Type: <b>HANDLE</b>


            The handle to the "device removed" event.
          


### -param pdwCookie [out]

Type: <b>DWORD*</b>


            A pointer to information about the "device removed" event, which can be used in <a href="https://msdn.microsoft.com/F1B8BBD2-3D7D-4125-953F-D10D073B77AF">UnregisterDeviceRemoved</a> to unregister the event. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>


            See <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.
          




## -remarks



Indicates when a Direct3D device has become removed for any reason, using an asynchronous notification mechanism, rather than as an HRESULT from <a href="https://msdn.microsoft.com/4214fa05-d876-420e-a125-c68d6c4e6801">Present</a>. The reason for device removal can be retrieved using <a href="https://msdn.microsoft.com/9e09c954-5c61-49fd-b25a-87dc0051a84d">ID3D11Device::GetDeviceRemovedReason</a> after being notified of the occurrence.


          Applications register and un-register a Win32 event handle with a particular device.
          That event handle will be signaled when the device becomes removed.
          A poll into the device's <b>ID3D11Device::GetDeviceRemovedReason</b> method indicates that the device is removed.
        


<a href="https://msdn.microsoft.com/102a0417-5a17-41ee-a470-132562ff51c5">ISignalableNotifier</a> or <a href="https://msdn.microsoft.com/ebd0ecad-a864-43cf-a1cb-e4c2d595ef81">SetThreadpoolWait</a> can be used by UWP apps.
        


          When the graphics device is lost, the app or title will receive the graphics event, so that the app or title knows that its graphics device is no longer valid and it is safe for the app or title to re-create its DirectX devices.
          In response to this event, the app or title needs to re-create its rendering device 
			 and pass it into a SetRenderingDevice  call on the composition graphics device objects.
        


          After setting this new rendering device, the app or title needs to redraw content of all the pre-existing surfaces 
			 after the composition graphics device's <b>OnRenderingDeviceReplaced</b> event is fired.
        


          This method supports Composition for device loss.
        


          The event is not signaled when it is most ideal to re-create.
          So, instead, we recommend iterating through the adapter ordinals and creating the first ordinal that will succeed.
        


          The application can register an event with the device.
          The application will be signaled when the device becomes removed.
        


          If the device is already removed, calls to <b>RegisterDeviceRemovedEvent</b> will signal the event immediately.
          No device-removed error code will be returned from <b>RegisterDeviceRemovedEvent</b>.
        


          Each "device removed" event is never signaled, or is signaled only once.
          These events are not signaled during device destruction.
          These events are unregistered during destruction.
        


          The semantics of <b>RegisterDeviceRemovedEvent</b> are similar to
          <a href="https://msdn.microsoft.com/9DCB6309-C1FF-403F-94E1-ABA769D18170">IDXGIFactory2::RegisterOcclusionStatusEvent</a>.
        




## -see-also




<a href="https://msdn.microsoft.com/C4971129-C879-470A-ACD7-910D9F522E8C">ID3D11Device4</a>



<a href="https://msdn.microsoft.com/F1B8BBD2-3D7D-4125-953F-D10D073B77AF">UnregisterDeviceRemoved</a>
 

 

