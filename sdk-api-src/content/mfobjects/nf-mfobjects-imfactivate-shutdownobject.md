---
UID: NF:mfobjects.IMFActivate.ShutdownObject
title: IMFActivate::ShutdownObject
author: windows-sdk-content
description: Shuts down the created object.
old-location: mf\imfactivate_shutdownobject.htm
tech.root: medfound
ms.assetid: 1f88ff31-5a91-4838-bfce-673a5a85c766
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: 1f88ff31-5a91-4838-bfce-673a5a85c766, IMFActivate interface [Media Foundation],ShutdownObject method, IMFActivate.ShutdownObject, IMFActivate::ShutdownObject, ShutdownObject, ShutdownObject method [Media Foundation], ShutdownObject method [Media Foundation],IMFActivate interface, mf.imfactivate_shutdownobject, mfobjects/IMFActivate::ShutdownObject
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfobjects.h
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
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFActivate.ShutdownObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFActivate::ShutdownObject


## -description



Shuts down the created object.




## -parameters






## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



If you create an object by calling <a href="https://msdn.microsoft.com/120b8070-6732-450d-8334-b3910f7bb4d2">IMFActivate::ActivateObject</a>, call <b>ShutdownObject</b> when you are done using the object.

The component that calls <a href="https://msdn.microsoft.com/120b8070-6732-450d-8334-b3910f7bb4d2">ActivateObject</a>—not the component that creates the activation object—is responsible for calling <b>ShutdownObject</b>. For example, in a typical playback application, the application creates activation objects for the media sinks, but the Media Session calls <b>ActivateObject</b>. Therefore the Media Session, not the application, calls <b>ShutdownObject</b>.

After <b>ShutdownObject</b> is called, the activation object releases all of its internal references to the created object. If you call <a href="https://msdn.microsoft.com/120b8070-6732-450d-8334-b3910f7bb4d2">ActivateObject</a> again, the activation object will create a new instance of the other object.




## -see-also




<a href="https://msdn.microsoft.com/767d5f1c-2b8d-43b6-916b-035129e93204">Activation Objects</a>



<a href="https://msdn.microsoft.com/c0936e3c-3cd1-4c1e-a336-2dee7d943963">IMFActivate</a>
 

 

