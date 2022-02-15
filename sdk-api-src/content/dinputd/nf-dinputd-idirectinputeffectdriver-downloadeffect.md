---
UID: NF:dinputd.IDirectInputEffectDriver.DownloadEffect
title: IDirectInputEffectDriver::DownloadEffect (dinputd.h)
description: The IDirectInputEffectDriver::DownloadEffect method sends an effect to the device.
helpviewer_keywords: ["DownloadEffect","DownloadEffect method [Human Input Devices]","DownloadEffect method [Human Input Devices]","IDirectInputEffectDriver interface","IDirectInputEffectDriver interface [Human Input Devices]","DownloadEffect method","IDirectInputEffectDriver.DownloadEffect","IDirectInputEffectDriver::DownloadEffect","di_ref_6f931ad9-9a30-45a6-aae5-0b10b1e4e4a7.xml","dinputd/IDirectInputEffectDriver::DownloadEffect","hid.idirectinputeffectdriver_downloadeffect"]
old-location: hid\idirectinputeffectdriver_downloadeffect.htm
tech.root: hid
ms.assetid: c10ee6f6-ed9e-45f9-b98d-db62d250a420
ms.date: 12/05/2018
ms.keywords: DownloadEffect, DownloadEffect method [Human Input Devices], DownloadEffect method [Human Input Devices],IDirectInputEffectDriver interface, IDirectInputEffectDriver interface [Human Input Devices],DownloadEffect method, IDirectInputEffectDriver.DownloadEffect, IDirectInputEffectDriver::DownloadEffect, di_ref_6f931ad9-9a30-45a6-aae5-0b10b1e4e4a7.xml, dinputd/IDirectInputEffectDriver::DownloadEffect, hid.idirectinputeffectdriver_downloadeffect
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectInputEffectDriver::DownloadEffect
 - dinputd/IDirectInputEffectDriver::DownloadEffect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dinputd.h
api_name:
 - IDirectInputEffectDriver.DownloadEffect
---

# IDirectInputEffectDriver::DownloadEffect


## -description

The <b>IDirectInputEffectDriver::DownloadEffect</b> method sends an effect to the device.

## -parameters

### -param unnamedParam1

Specifies the external joystick number being addressed.

### -param unnamedParam2

Specifies the <b>dwEffectId</b> member of the <a href="/windows/desktop/api/dinputd/ns-dinputd-dieffectattributes">DIEFFECTATTRIBUTES</a> structure associated with the effect the application is attempting to create. The DIEFFECTATTRIBUTES structure is stored in the registry under the corresponding effect registry key and can be any 32-bit value. DirectInput passes the 32-bit value to the driver with no interpretation.

### -param unnamedParam3

On entry, this parameter is a pointer to the handle of the effect being downloaded. If this parameter points to a zero, then a new effect is downloaded. On exit, this parameter is a pointer to a <b>DWORD </b> that contains the new effect handle. On failure, the <b>DWORD</b> pointed to by this parameter is set to zero if the effect is lost, or left alone if the effect is still valid with its old parameters. Note that zero is never a valid effect handle.

### -param unnamedParam4

Points to a DIEFFECT structure that describes the new effect. The axis and button values have been converted to object identifiers, which consist of the following: 





#### One type specifier:



##### DIDFT_RELAXIS



##### DIDFT_ABSAXIS



##### DIDFT_PSHBUTTON



##### DIDFT_TGLBUTTON



##### DIDFT_POV



#### One instance identifier:



##### DIDFT_MAKEINSTANCE(n)

Other bits in the object identifier are reserved and should be ignored. 

For example, 0x02000104 = DIDFT_PSHBUTTON | DIDFT_MAKEINSTANCE(1) | other stuff 

This value indicates that the effect uses button 1.

### -param unnamedParam5

Specifies which portions of the effect information have changed from the effect already applied to the device. This information is passed to drivers to allow for the optimization of effect modification. If an effect is being modified, a driver may be able to update the effect in its original position and transmit to the device only the information that has changed. Drivers are not, however, required to implement this optimization. All members in the DIEFFECT structure pointed to by the <i>peff</i> parameter are valid, and a driver may choose simply to update all parameters of the effect at each download. (For information about the DIEFFECT structure, see the DirectInput section of the stand alone DirectX SDK.) 

This parameter can be zero, one, or more of the following: 





#### DIEP_DURATION

Indicates the <b>dwDuration</b> member of the DIEFFECT structure is being downloaded for the first time or has changed since its last download. 



#### DIEP_SAMPLEPERIOD

Indicates the <b>dwSamplePeriod</b> member of the DIEFFECT structure is being downloaded for the first time or has changed since its last download. 



#### DIEP_GAIN

Indicates the <b>dwGain</b> member of the DIEFFECT structure is being downloaded for the first time or has changed since its last download. 



#### DIEP_TRIGGERBUTTON

Indicates the <b>dwTriggerButton</b> member of the DIEFFECT structure is being downloaded for the first time or has changed since its last download. 



#### DIEP_TRIGGERREPEATINTERVAL

Indicates the <b>dwTriggerRepeatInterval</b> member of the DIEFFECT structure is being downloaded for the first time or has changed since its last download. 



#### DIEP_AXES

Indicates the <b>cAxes</b> and <b>rgdwAxes</b> members of the DIEFFECT structure are being downloaded for the first time or have changed since their last download. 



#### DIEP_DIRECTION

Indicates the <b>cAxes</b> and <b>rglDirection</b> members of the DIEFFECT structure are being downloaded for the first time or have changed since their last download. (The <b>dwFlags</b> member of the DIEFFECT structure specifies, through DIEFF_CARTESIAN or DIEFF_POLAR, the coordinate system in which the values should be interpreted.) 



#### DIEP_ENVELOPE

Indicates the <b>lpEnvelope</b> member of the DIEFFECT structure is being downloaded for the first time or has changed since its last download. If this flag is set and the <b>lpEnvelope</b> member is a <b>NULL</b> pointer, then the effect is being created with no envelope, or the existing envelope is being deleted. 



#### DIEP_TYPESPECIFICPARAMS

Indicates the <b>cbTypeSpecificParams</b> and <b>lpTypeSpecificParams</b> members of the DIEFFECT structure are being downloaded for the first time or have changed since their last download. 



#### DIEP_START

Indicates that the effect is to be restarted from the beginning after the parameters of the effect have been updated. Note that the DIEP_NODOWNLOAD flag overrides the DIEP_START flag. 



#### DIEP_NORESTART

If this flag is not specified, the effect device driver is permitted to restart the effect if doing so is necessary to change the specified parameters. Note that the DIEP_NODOWNLOAD and DIEP_START flags override this flag. 



#### DIEP_NODOWNLOAD

Suppresses the automatic download that is normally performed after the parameters are updated. If this flag is set, the driver should validate parameters without performing an actual download.

## -returns

Returns S_OK if successful, or an error value otherwise.