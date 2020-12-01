---
UID: NS:winbase._COMMCONFIG
title: COMMCONFIG (winbase.h)
description: Contains information about the configuration state of a communications device.
helpviewer_keywords: ["*LPCOMMCONFIG","COMMCONFIG","COMMCONFIG structure","LPCOMMCONFIG","LPCOMMCONFIG structure pointer","_COMMCONFIG","_win32_commconfig_str","base.commconfig_str","winbase/COMMCONFIG","winbase/LPCOMMCONFIG"]
old-location: base\commconfig_str.htm
tech.root: base
ms.assetid: 9fd66f39-06a2-4159-9d1e-4ba84570c510
ms.date: 12/05/2018
ms.keywords: '*LPCOMMCONFIG, COMMCONFIG, COMMCONFIG structure, LPCOMMCONFIG, LPCOMMCONFIG structure pointer, _COMMCONFIG, _win32_commconfig_str, base.commconfig_str, winbase/COMMCONFIG, winbase/LPCOMMCONFIG'
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
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
req.typenames: COMMCONFIG, *LPCOMMCONFIG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _COMMCONFIG
 - winbase/_COMMCONFIG
 - LPCOMMCONFIG
 - winbase/LPCOMMCONFIG
 - COMMCONFIG
 - winbase/COMMCONFIG
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winbase.h
api_name:
 - COMMCONFIG
---

# COMMCONFIG structure


## -description

Contains information about the configuration state of a communications device.

## -struct-fields

### -field dwSize

The size of the structure, in bytes. The caller must set this member to <code>sizeof(COMMCONFIG)</code>.

### -field wVersion

The version number of the structure. This parameter can be 1. The version of the provider-specific structure should be included in the <b>wcProviderData</b> member.

### -field wReserved

Reserved; do not use.

### -field dcb

The device-control block (<a href="/windows/desktop/api/winbase/ns-winbase-dcb">DCB</a>) structure for RS-232 serial devices. A 
<b>DCB</b> structure is always present regardless of the port driver subtype specified in the device's 
<a href="/windows/desktop/api/winbase/ns-winbase-commprop">COMMPROP</a> structure.

### -field dwProviderSubType

The type of communications provider, and thus the format of the provider-specific data. For a list of communications provider types, see the description of the 
<a href="/windows/desktop/api/winbase/ns-winbase-commprop">COMMPROP</a> structure.

### -field dwProviderOffset

The offset of the provider-specific data relative to the beginning of the structure, in bytes. This member is zero if there is no provider-specific data.

### -field dwProviderSize

The size of the provider-specific data, in bytes.

### -field wcProviderData

Optional provider-specific data. This member can be of any size or can be omitted. Because the 
<b>COMMCONFIG</b> structure may be expanded in the future, applications should use the <b>dwProviderOffset</b> member to determine the location of this member.

## -remarks

If the provider subtype is PST_RS232 or PST_PARALLELPORT, the <b>wcProviderData</b> member is omitted. If the provider subtype is PST_MODEM, the <b>wcProviderData</b> member contains a 
<a href="/windows/desktop/api/mcx/ns-mcx-modemsettings">MODEMSETTINGS</a> structure.

## -see-also

<a href="/windows/desktop/api/winbase/ns-winbase-commprop">COMMPROP</a>



<a href="/windows/desktop/api/winbase/ns-winbase-dcb">DCB</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getcommproperties">GetCommProperties</a>



<a href="/windows/desktop/api/mcx/ns-mcx-modemsettings">MODEMSETTINGS</a>