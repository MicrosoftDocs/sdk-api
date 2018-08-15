---
UID: NS:wnvapi._WNV_OBJECT_HEADER
title: "_WNV_OBJECT_HEADER"
author: windows-sdk-content
description: Specifies the major version, minor version, and buffer size of the WNV_NOTIFICATION_PARAM structure that is passed to the WnvRequestNotification function.
old-location: wnv\wnv_object_header.htm
old-project: wnv
ms.assetid: 3D139C56-0224-4120-B308-A33F257DD9DC
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: "*PWNV_OBJECT_HEADER, PWNV_OBJECT_HEADER, PWNV_OBJECT_HEADER structure pointer [Windows Network Virtualization], WNV_OBJECT_HEADER, WNV_OBJECT_HEADER structure [Windows Network Virtualization], _WNV_OBJECT_HEADER, wnv.wnv_object_header, wnvapi/PWNV_OBJECT_HEADER, wnvapi/WNV_OBJECT_HEADER"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wnvapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WNV_OBJECT_HEADER, *PWNV_OBJECT_HEADER
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wnvapi.h
api_name:
 - WNV_OBJECT_HEADER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WNV_OBJECT_HEADER structure


## -description


Specifies the major version, minor version, and buffer size of the <a href="https://msdn.microsoft.com/C8A27B21-462A-4D70-AA19-743023FD1810">WNV_NOTIFICATION_PARAM</a> structure that is passed to the <a href="https://msdn.microsoft.com/CA0F9AAE-95E5-4A62-8A26-11F933B2D09E">WnvRequestNotification</a> function.


## -struct-fields




### -field MajorVersion

Type: <b>UCHAR</b>

The major version number. This value must be <b>WNV_API_MAJOR_VERSION_1</b>.


### -field MinorVersion

Type: <b>UCHAR</b>

The minor version number. This value must be <b>WNV_API_MINOR_VERSION_0</b>.


### -field Size

Type: <b>ULONG</b>

The size of the <b>Buffer</b> field in the <a href="https://msdn.microsoft.com/C8A27B21-462A-4D70-AA19-743023FD1810">WNV_NOTIFICATION_PARAM</a> structure that is passed to the <a href="https://msdn.microsoft.com/CA0F9AAE-95E5-4A62-8A26-11F933B2D09E">WnvRequestNotification</a> function.


## -remarks



There is currently only one version number: "1.0".



