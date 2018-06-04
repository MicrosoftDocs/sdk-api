---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
---

# MonthCal_GetMinReqRect macro


## -description


Retrieves the minimum size required to display a full month in a month calendar control. Size information is presented in the form of a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure. You can use this macro or send the <a href="https://msdn.microsoft.com/f0378338-4809-48e9-9387-ed8b79356f95">MCM_GETMINREQRECT</a> message explicitly. 


## -parameters




### -param hmc

TBD


### -param prc

TBD






#### - hwndMC

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to a month calendar control. 


#### - lpRectInfo

Type: <b>LPRECT</b>

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that will receive bounding rectangle information. This parameter must be a valid address and cannot be <b>NULL</b>. 


## -remarks



The minimum required window size for a month calendar control depends on the currently selected font, control styles, system metrics, and regional settings. When an application changes anything that affects the minimum window size, or processes a <a href="https://msdn.microsoft.com/77174e06-a25b-440a-9e9c-4fd5979c433c">WM_SETTINGCHANGE</a> message, it should call <b>MonthCal_GetMinReqRect</b> to determine the new minimum size.

<div class="alert"><b>Note</b>  The rectangle returned by <b>MonthCal_GetMinReqRect</b> does not include the width of the "Today" string, if it is present. If the <a href="Month_calendar_control_styles.htm">MCS_NOTODAY</a> style is not set, your application should also retrieve the rectangle that defines the "Today" string width by calling the <a href="https://msdn.microsoft.com/dcbbcf01-d4a5-4552-9b77-0681aaf6485f">MonthCal_GetMaxTodayWidth</a> macro. Use the larger of the two rectangles to ensure that the "Today" string is not clipped.</div>
<div> </div>
The <b>top</b> and <b>left</b> members of <i>lpRectInfo</i> will always be zero. The <b>right</b> and <b>bottom</b> members represent the minimum <i>cx</i> and <i>cy</i> required for the control.



