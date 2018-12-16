---
UID: NF:ddraw.IDirectDraw7.EvaluateMode
title: IDirectDraw7::EvaluateMode
author: windows-sdk-content
description: Used after a call to IDirectDraw7::StartModeTest to pass or fail each mode that the test presents and to step through the modes until the test is complete.
old-location: directdraw\idirectdraw7_evaluatemode.htm
tech.root: directdraw
ms.assetid: c8027183-07b5-4b7f-8c36-7bd711dac7dd
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DDEM_MODEFAILED, DDEM_MODEPASSED, EvaluateMode, EvaluateMode method [DirectDraw], EvaluateMode method [DirectDraw],IDirectDraw7 interface, IDirectDraw7 interface [DirectDraw],EvaluateMode method, IDirectDraw7.EvaluateMode, IDirectDraw7::EvaluateMode, ddraw/IDirectDraw7::EvaluateMode, directdraw.idirectdraw7_evaluatemode
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
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ddraw.dll
api_name:
 - IDirectDraw7.EvaluateMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectDraw7::EvaluateMode


## -description


Used after a call to <a href="https://msdn.microsoft.com/b669e3c7-b34b-4919-9a3e-0349288360ba">IDirectDraw7::StartModeTest</a> to pass or fail each mode that the test presents and to step through the modes until the test is complete.



## -parameters




### -param arg1 [in]

One of the following flags that indicate the status of the mode being tested:



#### DDEM_MODEPASSED

The mode being tested has passed.



#### DDEM_MODEFAILED

The mode being tested has failed.


### -param arg2 [out]

A pointer to a variable that receives a value that denotes the seconds that remain before the current mode is failed automatically unless it is explicitly passed or failed.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails or on completion, the method can return one of the following error values:

<ul>
<li>DDERR_TESTFINISHED</li>
<li>DDERR_NEWMODE</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_NOTFOUND </li>
</ul>



## -remarks



You can use <b>EvaluateMode</b> in conjunction with the <a href="https://msdn.microsoft.com/b669e3c7-b34b-4919-9a3e-0349288360ba">IDirectDraw7::StartModeTest</a> method to determine the maximum refresh rate that an EDID monitor and display adapter combination can support for each screen resolution.

Specifically, a call to <a href="https://msdn.microsoft.com/b669e3c7-b34b-4919-9a3e-0349288360ba">IDirectDraw7::StartModeTest</a> directs DirectDraw to establish a set of testable resolutions and to display a mode based on the first resolution in the set. Subsequent calls to <b>EvaluateMode</b> can be used to pass or fail each mode and to advance the test to the next display mode. The method steps through the testable resolutions starting with the highest refresh rate supported for a given resolution. After a refresh rate for a given resolution passes, testing of lower refresh rates for that resolution is skipped.



When the test is initiated, or whenever a mode is passed or failed, DirectDraw begins a 15 second timeout. An application can monitor the time remaining without passing or failing the current mode by calling <b>EvaluateMode</b> with a value of 0 for the dwFlags argument. Note that DirectDraw only changes modes or terminates the test when <b>EvaluateMode</b> is called. However, if an application calls <b>EvaluateMode</b> after the timeout period has elapsed, the current mode fails, regardless of the value passed to the <i>dwFlags</i> parameter.



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the  <b>EvaluateMode</b> method.




## -see-also




<a href="https://msdn.microsoft.com/1a1164fe-00c2-4469-8346-f86f7f48781e">IDirectDraw7</a>
 

 

