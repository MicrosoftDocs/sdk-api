---
UID: NF:dinputd.IDirectInputEffectDriver.GetVersions
title: IDirectInputEffectDriver::GetVersions
author: windows-sdk-content
description: The IDirectInputEffectDriver::GetVersions method obtains version information about the force-feedback hardware and driver.
old-location: hid\idirectinputeffectdriver_getversions.htm
tech.root: hid
ms.assetid: eda284d2-3e9c-436f-ad28-6397ff75d8ca
ms.author: windowssdkdev
ms.date: 10/02/2018
ms.keywords: GetVersions, GetVersions method [Human Input Devices], GetVersions method [Human Input Devices],IDirectInputEffectDriver interface, IDirectInputEffectDriver interface [Human Input Devices],GetVersions method, IDirectInputEffectDriver.GetVersions, IDirectInputEffectDriver::GetVersions, di_ref_edc7dd85-8838-4835-9987-54458f3c0bd6.xml, dinputd/IDirectInputEffectDriver::GetVersions, hid.idirectinputeffectdriver_getversions
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dinputd.h
req.include-header: Dinputd.h
req.target-type: Desktop
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dinputd.h
api_name:
 - IDirectInputEffectDriver.GetVersions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectInputEffectDriver::GetVersions


## -description


The <b>IDirectInputEffectDriver::GetVersions </b>method obtains version information about the force-feedback hardware and driver. 


## -parameters






#### - pvers

Points to a <a href="https://msdn.microsoft.com/28e24657-a75e-49d1-88b0-3e40ba8851ae">DIDRIVERVERSIONS</a> structure that should be filled in with version information describing the hardware, firmware, and driver. DirectInput sets the <b>dwSize</b> member of the DIDRIVERVERSIONS structure to <b>sizeof</b>(DIDRIVERVERSIONS) before calling this method. 


## -returns



Returns S_OK if successful; otherwise, returns an error code.



