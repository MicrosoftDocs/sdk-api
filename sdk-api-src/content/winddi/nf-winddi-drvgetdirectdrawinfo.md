---
UID: NF:winddi.DrvGetDirectDrawInfo
title: DrvGetDirectDrawInfo function
author: windows-sdk-content
description: The DrvGetDirectDrawInfo function returns the capabilities of the graphics hardware.
old-location: display\drvgetdirectdrawinfo.htm
old-project: display
ms.assetid: c6068572-bd73-4faa-b085-9608ebc450ea
ms.author: windowssdkdev
ms.date: 08/13/2018
ms.keywords: DrvGetDirectDrawInfo, DrvGetDirectDrawInfo function [Display Devices], ddfncs_bebc9a48-6664-4b23-908f-a4c586e79f63.xml, display.drvgetdirectdrawinfo, winddi/DrvGetDirectDrawInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.redist: 
req.target-type: Desktop
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
tech.root: 
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - DrvGetDirectDrawInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# DrvGetDirectDrawInfo function


## -description


The <b>DrvGetDirectDrawInfo</b> function returns the capabilities of the graphics hardware.


## -parameters




### -param dhpdev

Handle to the <a href="https://msdn.microsoft.com/139a10e9-203b-499b-9291-8537eae9189c">PDEV</a> returned by the driver's <a href="https://msdn.microsoft.com/9a7ed18a-f21c-486b-9261-59a3fe5aef9e">DrvEnablePDEV</a> routine.


### -param pHalInfo

Points to a <a href="https://msdn.microsoft.com/99ecd219-1e85-4904-867d-3efcb378bb11">DD_HALINFO</a> structure in which the driver should return the hardware capabilities that it supports.


### -param pdwNumHeaps

Points to the location in which the driver should return the number of VIDEOMEMORY structures pointed to by <i>pvmList</i>.


### -param pvmList

Points to an array of <a href="https://msdn.microsoft.com/a472a9f6-d85e-429b-9b0d-efce576b6330">VIDEOMEMORY</a> structures in which the driver should return information about each display memory chunk that it controls. The driver should ignore this parameter when it is <b>NULL</b>.


### -param pdwNumFourCCCodes

Points to the location in which the driver should return the number of DWORDs pointed to by <i>pdwFourCC</i>.


### -param pdwFourCC

Points to an array of DWORDs in which the driver should return information about each <a href="https://msdn.microsoft.com/f697e0db-1db0-4a81-94d8-0ca079885480">FOURCC</a> that it supports. The driver should ignore this parameter when it is <b>NULL</b>.


## -returns



<b>DrvGetDirectDrawInfo</b> returns <b>TRUE</b> if it succeeds; otherwise, it returns <b>FALSE</b>.




## -remarks



The driver's <b>DrvGetDirectDrawInfo</b> routine should do the following:

<ul>
<li>When <i>pvmList</i> and <i>pdwFourCC</i> are <b>NULL</b>:<ol>
<li>Reserve offscreen display memory for DirectDraw use.</li>
<li>Write the number of driver display memory heaps and supported FOURCCs in <i>pdwNumHeaps</i> and <i>pdwNumFourCC</i>, respectively.</li>
</ol>
</li>
<li>When <i>pvmList</i> and <i>pdwFourCC</i> are not <b>NULL</b>:<ol>
<li>Write the number of driver display memory heaps and supported FOURCCs in <i>pdwNumHeaps</i> and <i>pdwNumFourCC</i>, respectively.</li>
<li>For each <a href="https://msdn.microsoft.com/a472a9f6-d85e-429b-9b0d-efce576b6330">VIDEOMEMORY</a> structure in the list to which <i>pvmList</i> points, fill in the appropriate members to describe a particular chunk of display memory. The list of structures provides DirectDraw with a complete description of the driver's offscreen memory.</li>
</ol>
</li>
<li>Initialize the members of the <a href="https://msdn.microsoft.com/99ecd219-1e85-4904-867d-3efcb378bb11">DD_HALINFO</a> structure with driver-specific information as follows:<ol>
<li>Initialize the appropriate members of the <a href="https://msdn.microsoft.com/c5df8f26-3eb1-4743-96d1-7b73d902be8d">VIDEOMEMORYINFO</a> structure in <i>vmiData</i> to describe the general characteristics of the display's memory.</li>
<li>Initialize the appropriate members of the <a href="https://msdn.microsoft.com/529d60b5-658d-4d55-a599-fa35386c01a7">DDCORECAPS</a> structure in <b>ddCaps</b> to describe the capabilities of the hardware.</li>
<li>If the driver implements a <a href="https://msdn.microsoft.com/89a22163-a678-4c72-932a-ae4d17922e0b">DdGetDriverInfo</a> function, set <b>GetDriverInfo</b> to point to it and set <b>dwFlags</b> to DDHALINFO_GETDRIVERINFOSET.</li>
</ol>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/99ecd219-1e85-4904-867d-3efcb378bb11">DD_HALINFO</a>



<a href="https://msdn.microsoft.com/89a22163-a678-4c72-932a-ae4d17922e0b">DdGetDriverInfo</a>



<a href="https://msdn.microsoft.com/eb7e8775-d0ff-42af-8266-5171902eac22">DrvEnableDirectDraw</a>



<a href="https://msdn.microsoft.com/a472a9f6-d85e-429b-9b0d-efce576b6330">VIDEOMEMORY</a>



<a href="https://msdn.microsoft.com/c5df8f26-3eb1-4743-96d1-7b73d902be8d">VIDEOMEMORYINFO</a>
 

 

