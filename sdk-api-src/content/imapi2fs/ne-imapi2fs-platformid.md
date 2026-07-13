---
UID: NE:imapi2fs.PlatformId
title: PlatformId (imapi2fs.h)
description: Defines values for the operating system architecture that the boot image supports.
helpviewer_keywords: ["PlatformEFI","PlatformId","PlatformId enumeration [IMAPI]","PlatformMac","PlatformPowerPC","PlatformX86","imapi.platformid","imapi2fs/PlatformEFI","imapi2fs/PlatformId","imapi2fs/PlatformMac","imapi2fs/PlatformPowerPC","imapi2fs/PlatformX86"]
old-location: imapi\platformid.htm
tech.root: imapi
ms.assetid: 296f9da1-99be-4d20-8961-f99cf220404a
ms.date: 12/05/2018
ms.keywords: PlatformEFI, PlatformId, PlatformId enumeration [IMAPI], PlatformMac, PlatformPowerPC, PlatformX86, imapi.platformid, imapi2fs/PlatformEFI, imapi2fs/PlatformId, imapi2fs/PlatformMac, imapi2fs/PlatformPowerPC, imapi2fs/PlatformX86
req.header: imapi2fs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2fs.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: PlatformId
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PlatformId
 - imapi2fs/PlatformId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - imapi2fs.h
api_name:
 - PlatformId
---

# PlatformId enumeration


## -description

Defines values for the operating system architecture that the boot image supports

## -enum-fields

### -field PlatformX86:0

 Intel Pentium™ series of chip sets. This entry implies a Windows  operating system.

### -field PlatformPowerPC:1

Apple PowerPC family.

### -field PlatformMac:2

Apple Macintosh  family.

### -field PlatformEFI:0xef

EFI Family.

## -remarks

Other values not defined here may exist. Consumers of this enumeration should not presume this list to be the only set of valid values.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ibootoptions-get_platformid">IBootOptions::get_PlatformId</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ibootoptions-put_platformid">IBootOptions::put_PlatformId</a>
