---
UID: NN:locationapi.ILocation
title: ILocation (locationapi.h)
description: Provides methods used to manage location reports, event registration, and sensor permissions.
helpviewer_keywords: ["ILocation","ILocation interface [WinLocation]","ILocation interface [WinLocation]","described","locationapi/ILocation","winlocation.ilocation"]
old-location: winlocation\ilocation.htm
tech.root: winlocation
ms.assetid: beeedbbd-df93-4c05-a215-4cfd14e03076
ms.date: 12/05/2018
ms.keywords: ILocation, ILocation interface [WinLocation], ILocation interface [WinLocation],described, locationapi/ILocation, winlocation.ilocation
req.header: locationapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
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
req.dll: LocationAPI.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ILocation
 - locationapi/ILocation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - LocationAPI.dll
api_name:
 - ILocation
---

# ILocation interface


## -description

<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="/uwp/api/windows.devices.geolocation">Windows.Devices.Geolocation</a> API.
]

Provides methods used to manage location reports, event registration, and sensor permissions.

## -inheritance

The <b>ILocation</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ILocation</b> also has these types of members:

## -remarks

When <b>CoCreateInstance</b> is called to create an <b>ILocation</b> object, it may result in a notification being displayed in the taskbar, and a Location Activity event being logged in Event Viewer, if it is the application's first use of location.
