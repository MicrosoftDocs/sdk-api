---
UID: NF:sysinfoapi.GetLocalTime
title: GetLocalTime function
author: windows-driver-content
description: Gets the system time for a specific time zone.
old-location: sidebar\System_Time_getLocalTime.htm
old-project: sidebar
ms.assetid: VS|sidebar|~\sidebar\reference\objects\systemtime\getlocaltime.htm
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: GetLocalTime, System.Time object [Windows Sidebar], getLocalTime method, System.Time.getLocalTime, getLocalTime method [Windows Sidebar], getLocalTime method [Windows Sidebar], System.Time object, sidebar.System_Time_getLocalTime
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: sysinfoapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sidebar.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SyncProviderConfiguration
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Sidebar.Exe
api_name:
-	System.Time.getLocalTime
product: Windows
targetos: Windows
req.lib: 
req.dll: Sidebar.Exe (version 1.00 or later)
req.irql: 
req.product: Windows XP with SP1 and later
---

# GetLocalTime function


## -description


<p class="CCE_Message">[
The Windows Gadget Platform/Sidebar is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.
]



        Gets the system time for a specific time zone.
		


## -parameters




### -param lpSystemTime

TBD




#### - oTimeZone [in]


<a href="https://msdn.microsoft.com/68dcf69b-4d0b-4c44-9470-9f0bd7f6e8be">System.Time.timeZone</a> that specifies the desired time zone offset.
				


## -returns




            The system time, adjusted for time zone offset, as a <b>String</b>.
            




## -remarks




    Each <a href="https://msdn.microsoft.com/68dcf69b-4d0b-4c44-9470-9f0bd7f6e8be">System.Time.timeZone</a> in the <a href="https://msdn.microsoft.com/a763108e-11dd-4430-b743-e8aa87aedd1c">timeZones</a> collection corresponds to the system time zones itemized in the <b>Time Zone Settings</b> dialog.
        

The following image shows the Time Zone Settings dialog.

<img alt="Time Zone Settings dialog" src="images/Reference/TimeZoneSettings.PNG"/>

#### Examples


    The following example demonstrates how to get the local time based on a selected time zone.

<div class="code"><span codelanguage="JScript"><table>
<tr>
<th>JScript</th>
</tr>
<tr>
<td>
<pre>var oSelectedTimeZone = System.Time.currentTimeZone;
    
// --------------------------------------------------------------------
// Display the system time based on selected time zone.
// --------------------------------------------------------------------
function DisplayTime()
{
    // Retrieve the local time.
    var sTimeInfo = System.Time.getLocalTime(oSelectedTimeZone);
    if (sTimeInfo != "")
    {
        System.Sound.beep();
        var dDateInfo = new Date(Date.parse(sTimeInfo));   
        tHours = dDateInfo.getHours();
        tMinutes = dDateInfo.getMinutes();
        tMinutes = ((tMinutes &lt; 10) ? ":0" : ":") + tMinutes
        tSeconds = dDateInfo.getSeconds();
        tSeconds = ((tSeconds &lt; 10) ? ":0" : ":") + tSeconds;
        return tHours + tMinutes + tSeconds;
    }
    else
    {
        // Display default text.
    }
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/7e08e154-6c0a-433a-8f39-b9cf836c7976">DSTBias</a>



<a href="https://msdn.microsoft.com/2e9e2cd1-cbb4-4196-9d10-bc6904827296">DSTDate</a>



<a href="https://msdn.microsoft.com/7fdfc0de-8f96-45ea-8954-9d05b34fea0d">DSTDisplayName</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/09defa9c-0ba5-40e8-9ab9-35c2201c5005">System.Time</a>



<a href="https://msdn.microsoft.com/68dcf69b-4d0b-4c44-9470-9f0bd7f6e8be">System.Time.timeZone</a>



<a href="https://msdn.microsoft.com/c2be7e3c-ab6d-44dd-8e79-22423cbf90c7">bias</a>



<a href="https://msdn.microsoft.com/530b9cad-e215-4237-baca-ea0a785fb6d4">currentTimeZone</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh965535">displayName</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">name</a>



<a href="https://msdn.microsoft.com/5c8ffdb2-4e8d-484f-8033-ce7ab328a69f">standardBias</a>



<a href="https://msdn.microsoft.com/85c17936-3108-4831-957c-cd855cf79f2e">standardDate</a>



<a href="https://msdn.microsoft.com/a8b17a3c-16c0-4f7a-afd8-a2c70344d019">standardDisplayName</a>



<a href="https://msdn.microsoft.com/a763108e-11dd-4430-b743-e8aa87aedd1c">timeZones</a>
 

 

