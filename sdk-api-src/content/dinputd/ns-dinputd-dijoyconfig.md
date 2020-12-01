---
UID: NS:dinputd.DIJOYCONFIG
title: DIJOYCONFIG (dinputd.h)
description: The DIJOYCONFIG structure contains information about a joystick's configuration.
helpviewer_keywords: ["*LPDIJOYCONFIG","DIJOYCONFIG","DIJOYCONFIG structure [Human Input Devices]","di_ref_dc34a740-8987-4012-9e22-e59de2544445.xml","dinputd/DIJOYCONFIG","hid.dijoyconfig"]
old-location: hid\dijoyconfig.htm
tech.root: hid
ms.assetid: 2b17432f-fa5e-4ce3-9814-c24a45a49343
ms.date: 12/05/2018
ms.keywords: '*LPDIJOYCONFIG, DIJOYCONFIG, DIJOYCONFIG structure [Human Input Devices], di_ref_dc34a740-8987-4012-9e22-e59de2544445.xml, dinputd/DIJOYCONFIG, hid.dijoyconfig'
req.header: dinputd.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DIJOYCONFIG, *LPDIJOYCONFIG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DIJOYCONFIG
 - dinputd/DIJOYCONFIG
 - LPDIJOYCONFIG
 - dinputd/LPDIJOYCONFIG
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dinputd.h
api_name:
 - DIJOYCONFIG
---

# DIJOYCONFIG structure


## -description

The DIJOYCONFIG structure contains information about a joystick's configuration.

## -struct-fields

### -field dwSize

Specifies the size of the structure in bytes. This member must be initialized before the structure is used.

### -field guidInstance

Specifies the instance GUID for the joystick.

### -field hwc

Joystick hardware configuration.

### -field dwGain

Specifies the global gain setting. This value is applied to all force feedback effects as a "master volume control".

### -field wszType

The joystick type for the joystick. It must be one of the values enumerated by <a href="/windows/desktop/api/dinputd/nf-dinputd-idirectinputjoyconfig8-enumtypes">IDirectInputJoyConfig8::EnumTypes</a>.

### -field wszCallout

The callout driver for the joystick.

### -field guidGameport

Specifies a GUID that identifies the gameport being used for this joystick.

## -remarks

WDM gameports can be found during enumeration by calling <a href="/windows/desktop/api/dinputd/nf-dinputd-idirectinputjoyconfig8-gettypeinfo">IDirectInputJoyConfig8::GetTypeInfo</a> method for an enumerated joystick, then studying the flags present in the <b>dwFlags</b> member of the <a href="/windows/desktop/api/dinputd/ns-dinputd-dijoytypeinfo">DIJOYTYPEINFO</a> structure. If the JOY_HWS_ISGAMEPORTBUS flag is set, the currently enumerated object is an available WDM gameport.