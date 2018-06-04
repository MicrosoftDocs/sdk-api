---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# DXGI_OUTPUT_DESC structure


## -description


Describes an output or physical connection between the adapter (video card) and a device.


## -struct-fields




### -field DeviceName

Type: <b>WCHAR[32]</b>

A string that contains the name of the output device.


### -field DesktopCoordinates

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a></b>

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure containing the bounds of the output in desktop coordinates. Desktop coordinates depend on the dots per inch (DPI) of the desktop.
For info about writing DPI-aware Win32 apps, see <a href="https://msdn.microsoft.com/784e308d-904b-40ac-bf98-1a00fa1c9cf0">High DPI</a>.


### -field AttachedToDesktop

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

True if the output is attached to the desktop; otherwise, false.


### -field Rotation

Type: <b><a href="https://msdn.microsoft.com/fcf5bce5-dde1-4d3b-9786-2abf1e18d942">DXGI_MODE_ROTATION</a></b>

A member of the <a href="https://msdn.microsoft.com/fcf5bce5-dde1-4d3b-9786-2abf1e18d942">DXGI_MODE_ROTATION</a> enumerated type describing on how an image is rotated by the output.


### -field Monitor

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HMONITOR</a></b>

An <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HMONITOR</a> handle that represents the display monitor. For more information, see <a href="https://msdn.microsoft.com/c43c1401-52d3-485e-a418-205df5737040">HMONITOR and the Device Context</a>.


## -remarks



The <b>DXGI_OUTPUT_DESC</b> structure is initialized by the <a href="https://msdn.microsoft.com/2ed41c7b-7b9b-49a1-a11d-9a94adee7824">IDXGIOutput::GetDesc</a> method.




## -see-also




<a href="https://msdn.microsoft.com/22e98880-bcd1-448a-9223-604fff9173fe">DXGI Structures</a>
 

 

