---
UID: NS:wnvapi._WNV_OBJECT_HEADER
title: WNV_OBJECT_HEADER (wnvapi.h)
description: Specifies the major version, minor version, and buffer size of the WNV_NOTIFICATION_PARAM structure that is passed to the WnvRequestNotification function.
helpviewer_keywords: ["*PWNV_OBJECT_HEADER","PWNV_OBJECT_HEADER","PWNV_OBJECT_HEADER structure pointer [Windows Network Virtualization]","WNV_OBJECT_HEADER","WNV_OBJECT_HEADER structure [Windows Network Virtualization]","wnv.wnv_object_header","wnvapi/PWNV_OBJECT_HEADER","wnvapi/WNV_OBJECT_HEADER"]
old-location: wnv\wnv_object_header.htm
tech.root: wnv
ms.assetid: 3D139C56-0224-4120-B308-A33F257DD9DC
ms.date: 12/05/2018
ms.keywords: '*PWNV_OBJECT_HEADER, PWNV_OBJECT_HEADER, PWNV_OBJECT_HEADER structure pointer [Windows Network Virtualization], WNV_OBJECT_HEADER, WNV_OBJECT_HEADER structure [Windows Network Virtualization], wnv.wnv_object_header, wnvapi/PWNV_OBJECT_HEADER, wnvapi/WNV_OBJECT_HEADER'
req.header: wnvapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: WNV_OBJECT_HEADER, *PWNV_OBJECT_HEADER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WNV_OBJECT_HEADER
 - wnvapi/_WNV_OBJECT_HEADER
 - PWNV_OBJECT_HEADER
 - wnvapi/PWNV_OBJECT_HEADER
 - WNV_OBJECT_HEADER
 - wnvapi/WNV_OBJECT_HEADER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wnvapi.h
api_name:
 - WNV_OBJECT_HEADER
---

# WNV_OBJECT_HEADER structure


## -description

Specifies the major version, minor version, and buffer size of the <a href="/windows/desktop/api/wnvapi/ns-wnvapi-wnv_notification_param">WNV_NOTIFICATION_PARAM</a> structure that is passed to the <a href="/previous-versions/windows/desktop/api/wnvapi/nf-wnvapi-wnvrequestnotification">WnvRequestNotification</a> function.

## -struct-fields

### -field MajorVersion

Type: <b>UCHAR</b>

The major version number. This value must be <b>WNV_API_MAJOR_VERSION_1</b>.

### -field MinorVersion

Type: <b>UCHAR</b>

The minor version number. This value must be <b>WNV_API_MINOR_VERSION_0</b>.

### -field Size

Type: <b>ULONG</b>

The size of the <b>Buffer</b> field in the <a href="/windows/desktop/api/wnvapi/ns-wnvapi-wnv_notification_param">WNV_NOTIFICATION_PARAM</a> structure that is passed to the <a href="/previous-versions/windows/desktop/api/wnvapi/nf-wnvapi-wnvrequestnotification">WnvRequestNotification</a> function.

## -remarks

There is currently only one version number: "1.0".