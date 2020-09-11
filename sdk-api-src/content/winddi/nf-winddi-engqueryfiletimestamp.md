---
UID: NF:winddi.EngQueryFileTimeStamp
title: EngQueryFileTimeStamp function (winddi.h)
description: The EngQueryFileTimeStamp function returns the time stamp of a file.
helpviewer_keywords: ["EngQueryFileTimeStamp","EngQueryFileTimeStamp function [Display Devices]","display.engqueryfiletimestamp","gdifncs_6f6a0fd0-d012-4f50-a686-7c58cc051c5a.xml","winddi/EngQueryFileTimeStamp"]
old-location: display\engqueryfiletimestamp.htm
tech.root: display
ms.assetid: f229c358-5c8d-4579-b6a6-f6bf1d12190b
ms.date: 12/05/2018
ms.keywords: EngQueryFileTimeStamp, EngQueryFileTimeStamp function [Display Devices], display.engqueryfiletimestamp, gdifncs_6f6a0fd0-d012-4f50-a686-7c58cc051c5a.xml, winddi/EngQueryFileTimeStamp
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EngQueryFileTimeStamp
 - winddi/EngQueryFileTimeStamp
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
api_name:
 - EngQueryFileTimeStamp
---

# EngQueryFileTimeStamp function


## -description

The <b>EngQueryFileTimeStamp</b> function returns the time stamp of a file.

## -parameters

### -param pwsz [in]

Pointer to a null-terminated string containing the name of the file to be queried.

## -returns

<b>EngQueryFileTimeStamp</b> returns the last time the file was written to upon success. It returns <b>NULL</b> if it fails.

## -remarks

The time returned is local system time for the current time zone, specified in system-time format. Absolute system time is the number of 100-nanosecond intervals since the start of 1601.

