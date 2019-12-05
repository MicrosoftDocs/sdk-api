---
UID: NS:dinputd.DIHIDFFINITINFO
title: DIHIDFFINITINFO (dinputd.h)
description: The DIHIDFFINITINFO structure is used by DirectInput to provide information to a HID force-feedback driver about the device it is being asked to control.
old-location: hid\dihidffinitinfo.htm
tech.root: hid
ms.assetid: 7eaf2d1e-f216-4678-9c8f-e6c38f6e4e66
ms.date: 12/05/2018
ms.keywords: '*LPDIHIDFFINITINFO, DIHIDFFINITINFO, DIHIDFFINITINFO structure [Human Input Devices], di_ref_2ed2499d-7d1f-4247-be74-ea356144df44.xml, dinputd/DIHIDFFINITINFO, hid.dihidffinitinfo'
ms.topic: struct
f1_keywords:
- dinputd/DIHIDFFINITINFO
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Dinputd.h
api_name:
- DIHIDFFINITINFO
targetos: Windows
req.typenames: DIHIDFFINITINFO, *LPDIHIDFFINITINFO
req.redist: 
ms.custom: 19H1
---

# DIHIDFFINITINFO structure


## -description


The <b>DIHIDFFINITINFO</b> structure is used by DirectInput to provide information to a HID force-feedback driver about the device it is being asked to control.


## -struct-fields




### -field dwSize

Specifies the size of the structure in bytes. This member must be initialized before the structure is used. 


### -field pwszDeviceInterface

Points to a null-terminated Unicode string that identifies the device interface for the device. The driver can pass the device interface to the <a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function to obtain access to the device.


### -field GuidInstance

Specifies a device instance GUID for this device.

