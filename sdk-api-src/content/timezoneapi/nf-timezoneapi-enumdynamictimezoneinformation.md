---
UID: NF:timezoneapi.EnumDynamicTimeZoneInformation
title: EnumDynamicTimeZoneInformation function
author: windows-sdk-content
description: Enumerates DYNAMIC_TIME_ZONE_INFORMATION entries stored in the registry.
old-location: base\enumdynamictimezoneinformation.htm
tech.root: sysinfo
ms.assetid: EBB2366A-86FE-4764-B7F9-5D305993CE0A
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: EnumDynamicTimeZoneInformation, EnumDynamicTimeZoneInformation function, base.enumdynamictimezoneinformation, timezoneapi/EnumDynamicTimeZoneInformation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: timezoneapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-TimeZone-l1-1-0.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - advapi32.dll
api_name:
 - EnumDynamicTimeZoneInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EnumDynamicTimeZoneInformation function


## -description


Enumerates <a href="https://msdn.microsoft.com/d60b1212-26bc-4fad-afce-9bd9062ca5b0">DYNAMIC_TIME_ZONE_INFORMATION</a> entries stored in the  registry. This information is used to support time zones that experience annual boundary changes due to daylight saving time adjustments. Use the information returned by this function when calling <a href="https://msdn.microsoft.com/6705BF71-9FF9-4D1F-B34B-752D9C83C964">GetDynamicTimeZoneInformationEffectiveYears</a> to retrieve the specific range of years to pass to <a href="https://msdn.microsoft.com/5bd29a25-98f0-439e-be88-8011bbf98926">GetTimeZoneInformationForYear</a>.


## -parameters




### -param dwIndex [in]

Index value that represents the location of a <a href="https://msdn.microsoft.com/d60b1212-26bc-4fad-afce-9bd9062ca5b0">DYNAMIC_TIME_ZONE_INFORMATION</a> entry.


### -param lpTimeZoneInformation [out]

Specifies settings for  a time zone and dynamic daylight saving time.


## -see-also




<a href="https://msdn.microsoft.com/d60b1212-26bc-4fad-afce-9bd9062ca5b0">DYNAMIC_TIME_ZONE_INFORMATION</a>



<a href="https://msdn.microsoft.com/6705BF71-9FF9-4D1F-B34B-752D9C83C964">GetDynamicTimeZoneInformationEffectiveYears</a>
 

 

