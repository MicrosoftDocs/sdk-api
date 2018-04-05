---
UID: NF:utilapiset.Beep
title: Beep function
author: windows-driver-content
description: Plays a simple waveform sound.
old-location: sidebar\System_Sound_beep.htm
old-project: sidebar
ms.assetid: VS|sidebar|~\sidebar\reference\objects\systemsound\beep.htm
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: Beep, System.Sound object [Windows Sidebar], beep method, System.Sound.beep, beep method [Windows Sidebar], beep method [Windows Sidebar], System.Sound object, sidebar.System_Sound_beep
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: utilapiset.h
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
req.typenames: TEXTRANGE_PROPERTIES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Sidebar.Exe
api_name:
-	System.Sound.beep
product: Windows
targetos: Windows
req.lib: 
req.dll: Sidebar.Exe (version 1.00 or later)
req.irql: 
req.product: Windows UI
---

# Beep function


## -description


<p class="CCE_Message">[
The Windows Gadget Platform/Sidebar is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.
]


Plays a simple waveform sound.
		


## -parameters




### -param dwFreq

TBD


### -param dwDuration

TBD




## -returns



This method does not return a value.




## -remarks




            After queuing the sound, control is returned to the calling function and the sound plays asynchronously.
            


			Muting and volume control have no effect on <b>System.Sound.beep</b>.

			


#### Examples


The following example demonstrates how to play the beep sound every second.


<div class="code"><span codelanguage="JScript"><table>
<tr>
<th>JScript</th>
</tr>
<tr>
<td>
<pre>var tHours;
var tMinutes;
var tSeconds;
var oSelectedTimeZone = System.Time.currentTimeZone;

// --------------------------------------------------------------------
// Initialize the gadget.
// --------------------------------------------------------------------
function Init()
{    
    // Initialize the time display.
    DisplayTime();
    setInterval("DisplayTime()",1000);
}

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
        timeDisplay.innerHTML = tHours + tMinutes + tSeconds;
    }
    else
    {
        // Display something else.
    }
}

</pre>
</td>
</tr>
</table></span></div>


