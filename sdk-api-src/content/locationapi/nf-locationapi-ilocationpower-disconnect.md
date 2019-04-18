---
UID: NF:locationapi.ILocationPower.Disconnect
title: ILocationPower::Disconnect (locationapi.h)
author: windows-sdk-content
description: Used by Windows Store app browsers in Windows 8 to notify the location platform that an app has been suspended (disconnect) and restored (connect).
old-location: winlocation_com_ref\ilocationpower_disconnect.htm
tech.root: locationapi
ms.assetid: 8bf9bc29-4e81-4d80-8de5-317678b34792
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Disconnect, Disconnect method [WinLocation], Disconnect method [WinLocation],ILocationPower interface, ILocationPower interface [WinLocation],Disconnect method, ILocationPower.Disconnect, ILocationPower::Disconnect, WinLocation_COM_Ref.ilocationpower_disconnect, locationapi/ILocationPower::Disconnect, winlocation.ilocationpower_disconnect
ms.topic: method
req.header: locationapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: LocationApi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: LocationAPI.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - LocationAPI.dll
api_name:
 - ILocationPower.Disconnect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ILocationPower::Disconnect


## -description


<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/fd40bf4a-c59a-43a4-ab01-c671a8a41731">Windows.Devices.Geolocation</a>API.
]

Used by Windows Store app browsers in Windows 8 to notify the location platform that an app has been suspended (disconnect) and restored (connect).

Most apps will not need to use this method.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/bf0a0c13-a50f-4ed8-bc29-7d70561da306">ILocationPower</a>
 

 

