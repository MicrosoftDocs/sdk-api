---
UID: NF:wiadevd.DeviceDialog
title: DeviceDialog function
author: windows-driver-content
description: Used by applications to display a device dialog box to the user.
old-location: wia\_wia_devicedialog.htm
old-project: wia
ms.assetid: VS|wia|~\wia\refwia\functions\devicedialog.htm
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: DeviceDialog, DeviceDialog function [WIA], _wia_devicedialog, wia._wia_devicedialog, wiadevd/DeviceDialog
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wiadevd.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WIA_RAW_HEADER, *PWIA_RAW_HEADER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	LibDef
api_location:
-	Wiaguid.lib
-	Wiaguid.dll
api_name:
-	DeviceDialog
product: Windows
targetos: Windows
req.lib: Wiaguid.lib
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# DeviceDialog function


## -description


Used by applications to display a device dialog box to the user.


## -parameters




### -param pDeviceDialogData [in]

Type: <b>PDEVICEDIALOGDATA</b>

The <a href="https://msdn.microsoft.com/library/windows/hardware/ff540560">DEVICEDIALOGDATA</a> to use to create the device dialog.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff540560">DEVICEDIALOGDATA</a>
 

 

