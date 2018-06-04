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

# IWiaItem::DeviceCommand


## -description


The <b>IWiaItem::DeviceCommand</b> issues a command to a Windows Image Acquisition (WIA) hardware device.


## -parameters




### -param lFlags [in]

Type: <b>LONG</b>

Currently unused. Should be set to zero.


### -param pCmdGUID [in]

Type: <b>const GUID*</b>

Specifies a unique identifier that specifies the command to send to the WIA hardware device. For a list of valid device commands, see <a href="https://msdn.microsoft.com/f86a0944-2f2a-467e-a9e8-4cdecfc50175">WIA Device Commands</a>.


### -param pIWiaItem [in, out]

Type: <b><a href="https://msdn.microsoft.com/b9aaf7ae-7222-44d1-8cf1-89234b263135">IWiaItem</a>**</b>

On output, this pointer points to the item created by the command, if any.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Applications use this method to send WIA commands to hardware devices. 

When the application sends the WIA_CMD_TAKE_PICTURE command to the device, <b>IWiaItem::DeviceCommand</b>, the WIA run-time system creates the <a href="https://msdn.microsoft.com/b9aaf7ae-7222-44d1-8cf1-89234b263135">IWiaItem</a> object to represent the image. The <b>IWiaItem::DeviceCommand</b> method stores the address of the interface in the <i>pIWiaItem</i>  parameter. 

Applications must call the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> method on the interface pointers they receive through the <i>pIWiaItem</i> parameter.



