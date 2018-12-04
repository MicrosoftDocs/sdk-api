---
UID: NF:shobjidl.IBandHost.SetBandAvailability
title: IBandHost::SetBandAvailability
author: windows-sdk-content
description: Sets the availability of a specified band.
old-location: shell\IBandHost_SetBandAvailability.htm
tech.root: shell
ms.assetid: a3e41e8f-45dd-4160-8a65-ec82b7e9abe7
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: IBandHost interface [Windows Shell],SetBandAvailability method, IBandHost.SetBandAvailability, IBandHost::SetBandAvailability, SetBandAvailability, SetBandAvailability method [Windows Shell], SetBandAvailability method [Windows Shell],IBandHost interface, _shell_IBandHost_SetBandAvailability, shell.IBandHost_SetBandAvailability, shobjidl/IBandHost::SetBandAvailability
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - Shobjidl.h
api_name:
 - IBandHost.SetBandAvailability
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBandHost::SetBandAvailability


## -description


Sets the availability of a specified band.


## -parameters




### -param rclsidBand [in]

Type: <b>REFCLSID</b>

A reference to a CLSID.


### -param fAvailable [in]

Type: <b>BOOL</b>

Specifies band availability.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



