---
UID: NF:ddraw.IDirectDraw7.StartModeTest
title: IDirectDraw7::StartModeTest
author: windows-sdk-content
description: Initiates a test to update the system registry with refresh rate information for the current display adapter and monitor combination.
old-location: directdraw\idirectdraw7_startmodetest.htm
old-project: directdraw
ms.assetid: b669e3c7-b34b-4919-9a3e-0349288360ba
ms.author: windowssdkdev
ms.date: 06/18/2018
ms.keywords: IDirectDraw7 interface [DirectDraw],StartModeTest method, IDirectDraw7.StartModeTest, IDirectDraw7::StartModeTest, StartModeTest, StartModeTest method [DirectDraw], StartModeTest method [DirectDraw],IDirectDraw7 interface, ddraw/IDirectDraw7::StartModeTest, directdraw.idirectdraw7_startmodetest
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: ddraw.h
req.include-header: 
req.target-type: Windows
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
req.typenames: DEDUP_CONTAINER_EXTENT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ddraw.dll
api_name:
 - IDirectDraw7.StartModeTest
product: Windows
targetos: Windows
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
---

# IDirectDraw7::StartModeTest


## -description


Initiates a test to update the system registry with refresh rate information for the current display adapter and monitor combination. A call to this method is typically followed by calls to <a href="https://msdn.microsoft.com/c8027183-07b5-4b7f-8c36-7bd711dac7dd">IDirectDraw7::EvaluateMode</a> to pass or fail modes displayed by the test.



## -parameters




### -param






#### - dwFlags [in]

Flags that specify options for starting a test. The only flag value that is currently valid is DDSMT_ISTESTREQUIRED. When this flag is specified, <b>StartModeTest</b> does not initiate a test, but instead returns a value that indicates whether it is possible or necessary to test the resolutions that the <i>lpModesToTest</i> and <i>dwNumEntries</i> parameters identify.


#### - dwNumEntries [in]

The number of elements in the array that the  <i>lpModesToTest</i> parameter specifies.


#### - lpModesToTest [in]

An array of SIZE elements that describe, in terms of screen resolutions, the modes that should be tested.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_CURRENTLYNOTAVAIL</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_NOEXCLUSIVEMODE</li>
<li>DDERR_NOTFOUND</li>
<li>DDERR_TESTFINISHED</li>
</ul>
When the method is called with the DDSMT_ISTESTREQUIRED flag, it can return one of the following values:

<ul>
<li>DDERR_NEWMODE</li>
<li>DDERR_NODRIVERSUPPORT</li>
<li>DDERR_NOMONITORINFORMATION</li>
<li>DDERR_TESTFINISHED</li>
</ul>



## -remarks



You can use the <b>StartModeTest</b> method together with the <a href="https://msdn.microsoft.com/c8027183-07b5-4b7f-8c36-7bd711dac7dd">IDirectDraw7::EvaluateMode</a> method to determine the maximum refresh rate that an EDID monitor and display adapter combination can support for each screen resolution. The results of the testing are stored in the system registry and affect the operation of <a href="https://msdn.microsoft.com/04ed2545-c611-435d-95ef-a0d854380a69">IDirectDraw7::EnumDisplayModes</a> when that method is called with the DDEDM_REFRESHRATES flag set.



Specifically, a call to <b>StartModeTest</b> directs DirectDraw to establish a set of testable resolutions and to display a mode based on the first resolution in the set. Subsequent calls to <a href="https://msdn.microsoft.com/c8027183-07b5-4b7f-8c36-7bd711dac7dd">IDirectDraw7::EvaluateMode</a> can be used to pass or fail each mode and to advance the test to the next display mode.



<b>StartModeTest</b> succeeds only with monitors that contain EDID data. If the monitor is not EDID-compliant, <b>StartModeTest</b> returns DDERR_TESTFINISHED without testing any modes. If the EDID table does not contain values higher than 60 Hz, no modes are tested. Refresh rates higher than 100 Hz are tested only if the EDID table contains values higher than 85 Hz.



If you call <b>StartModeTest</b> with an argument list of (NULL, 0, 0), <b>StartModeTest</b> clears existing refresh rate information from the registry.



The test does not guarantee to display only the resolutions in the array described by the <i>lpModesToTest</i> and <i>dwNumEntries</i> parameters. For example, the 640×480 resolution is used to obtain a maximum viewable refresh rate for the 320×200 resolution.



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the <b>StartModeTest</b> method.




## -see-also




<a href="https://msdn.microsoft.com/1a1164fe-00c2-4469-8346-f86f7f48781e">IDirectDraw7</a>
 

 

