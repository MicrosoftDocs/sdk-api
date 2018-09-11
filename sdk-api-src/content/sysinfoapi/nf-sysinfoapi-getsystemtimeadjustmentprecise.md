---
UID: NF:sysinfoapi.GetSystemTimeAdjustmentPrecise
title: GetSystemTimeAdjustmentPrecise function
author: windows-sdk-content
description: Determines whether the system is applying periodic, programmed time adjustments to its time-of-day clock, and obtains the value and period of any such adjustments.
old-location: base\getsystemtimeadjustmentprecise.htm
tech.root: SysInfo
ms.assetid: 95EEE23D-01D8-49E1-BA64-49C07E8B1619
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetSystemTimeAdjustmentPrecise, GetSystemTimeAdjustmentPrecise function, base.getsystemtimeadjustmentprecise, sysinfoapi/GetSystemTimeAdjustmentPrecise
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: sysinfoapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mincore.lib
req.dll: Api-ms-win-core-version-l1-2-3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Api-ms-win-core-version-l1-2-3.dll
api_name:
 - GetSystemTimeAdjustmentPrecise
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetSystemTimeAdjustmentPrecise function


## -description


Determines whether the system is applying periodic, programmed time adjustments to its time-of-day clock, and obtains the value and period of any such adjustments.


## -parameters




### -param lpTimeAdjustment [out]

Returns the adjusted clock update frequency.


### -param lpTimeIncrement [out]

Returns the clock update frequency.


### -param lpTimeAdjustmentDisabled [out]

Returns an indicator which specifies whether the time adjustment is enabled.

A value of <b>TRUE</b> indicates that periodic adjustment is disabled. In this case, the system may attempt to keep the time-of-day clock in sync using its own internal mechanisms. This may cause time-of-day to periodically jump to the "correct time."

A value of <b>FALSE</b> indicates that periodic, programmed time adjustment is being used to serialize time-of-day, and the system will not interfere or attempt to synchronize time-of-day on its own.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function is used in algorithms that  synchronize the time-of-day with another time source, using a programmed clock adjustment. To do this, the system computes the adjusted clock update frequency, and then this function allows the caller to obtain that value.


<div class="alert"><b>Note</b>  <p class="note">For a complete code sample on how to enable system-time privileges, adjust the system clock, and display clock values, see  <a href="base.SetSystemTimeAdjustmentPrecise">SetSystemTimeAdjustmentPrecise</a>.

</div>
<div> </div>





## -see-also




<a href="base.SetSystemTimeAdjustmentPrecise">SetSystemTimeAdjustmentPrecise</a>
 

 

