---
UID: NS:wtsapi32._WTS_CLIENT_DISPLAY
title: WTS_CLIENT_DISPLAY (wtsapi32.h)
description: Contains information about the display of a Remote Desktop Connection (RDC) client. (WTS_CLIENT_DISPLAY)
helpviewer_keywords: ["*PWTS_CLIENT_DISPLAY","1","16","2","24","32","4","8","PWTS_CLIENT_DISPLAY","PWTS_CLIENT_DISPLAY structure pointer [Remote Desktop Services]","WTS_CLIENT_DISPLAY","WTS_CLIENT_DISPLAY structure [Remote Desktop Services]","_win32_wts_client_display_str","termserv.wts_client_display_str","wtsapi32/PWTS_CLIENT_DISPLAY","wtsapi32/WTS_CLIENT_DISPLAY"]
old-location: termserv\wts_client_display_str.htm
tech.root: TermServ
ms.assetid: 0d5e0a9d-23b0-4302-ade3-eb9fbd7f787d
ms.date: 12/05/2018
ms.keywords: '*PWTS_CLIENT_DISPLAY, 1, 16, 2, 24, 32, 4, 8, PWTS_CLIENT_DISPLAY, PWTS_CLIENT_DISPLAY structure pointer [Remote Desktop Services], WTS_CLIENT_DISPLAY, WTS_CLIENT_DISPLAY structure [Remote Desktop Services], _win32_wts_client_display_str, termserv.wts_client_display_str, wtsapi32/PWTS_CLIENT_DISPLAY, wtsapi32/WTS_CLIENT_DISPLAY'
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
req.typenames: WTS_CLIENT_DISPLAY, *PWTS_CLIENT_DISPLAY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WTS_CLIENT_DISPLAY
 - wtsapi32/_WTS_CLIENT_DISPLAY
 - PWTS_CLIENT_DISPLAY
 - wtsapi32/PWTS_CLIENT_DISPLAY
 - WTS_CLIENT_DISPLAY
 - wtsapi32/WTS_CLIENT_DISPLAY
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
 - WTS_CLIENT_DISPLAY
---

# WTS_CLIENT_DISPLAY structure


## -description

Contains information about the display of a Remote Desktop Connection (RDC) client.

## -struct-fields

### -field HorizontalResolution

Horizontal dimension, in pixels, of the client's display.

### -field VerticalResolution

Vertical dimension, in pixels, of the client's display.

### -field ColorDepth

Color depth of the client's display. This member can be one of the following values.



#### 1

4 bits per pixel.



#### 2

8 bits per pixel.



#### 4

16 bits per pixel.



#### 8

A 3-byte RGB values for a maximum of 2^24 colors.



#### 16

15 bits per pixel.



#### 24

24 bits per pixel.



#### 32

32 bits per pixel.

## -see-also

<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsquerysessioninformationa">WTSQuerySessionInformation</a>
