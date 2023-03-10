---
UID: NE:wtsapi32._WTS_VIRTUAL_CLASS
title: WTS_VIRTUAL_CLASS (wtsapi32.h)
description: Contains values that indicate the type of virtual channel information to retrieve.
helpviewer_keywords: ["WTSVirtualClientData","WTSVirtualFileHandle","WTS_VIRTUAL_CLASS","WTS_VIRTUAL_CLASS enumeration [Remote Desktop Services]","_win32_wts_virtual_class","termserv.wts_virtual_class","wtsapi32/WTSVirtualClientData","wtsapi32/WTSVirtualFileHandle","wtsapi32/WTS_VIRTUAL_CLASS"]
old-location: termserv\wts_virtual_class.htm
tech.root: TermServ
ms.assetid: ca7bb0ff-f5af-477f-a610-563071554234
ms.date: 12/05/2018
ms.keywords: WTSVirtualClientData, WTSVirtualFileHandle, WTS_VIRTUAL_CLASS, WTS_VIRTUAL_CLASS enumeration [Remote Desktop Services], _win32_wts_virtual_class, termserv.wts_virtual_class, wtsapi32/WTSVirtualClientData, wtsapi32/WTSVirtualFileHandle, wtsapi32/WTS_VIRTUAL_CLASS
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: WTS_VIRTUAL_CLASS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WTS_VIRTUAL_CLASS
 - wtsapi32/_WTS_VIRTUAL_CLASS
 - WTS_VIRTUAL_CLASS
 - wtsapi32/WTS_VIRTUAL_CLASS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wtsapi32.h
api_name:
 - WTS_VIRTUAL_CLASS
---

# WTS_VIRTUAL_CLASS enumeration


## -description

Contains values that indicate the type of virtual channel information to retrieve.

## -enum-fields

### -field WTSVirtualClientData

This value is not currently supported.

### -field WTSVirtualFileHandle

Indicates a request for the file handle of a virtual channel that can be used for asynchronous I/O.

## -remarks

For an example that shows the use of the WTSVirtualFileHandle value, see <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsvirtualchannelquery">WTSVirtualChannelQuery</a>. This example shows how to gain access to a virtual channel file handle that can be used for asynchronous I/O.

## -see-also

<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsvirtualchannelquery">WTSVirtualChannelQuery</a>