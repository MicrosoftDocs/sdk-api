---
UID: NF:ddraw.IDirectDraw7.StartModeTest
title: IDirectDraw7::StartModeTest (ddraw.h)
description: Initiates a test to update the system registry with refresh rate information for the current display adapter and monitor combination.
helpviewer_keywords: ["IDirectDraw7 interface [DirectDraw]","StartModeTest method","IDirectDraw7.StartModeTest","IDirectDraw7::StartModeTest","StartModeTest","StartModeTest method [DirectDraw]","StartModeTest method [DirectDraw]","IDirectDraw7 interface","ddraw/IDirectDraw7::StartModeTest","directdraw.idirectdraw7_startmodetest"]
old-location: directdraw\idirectdraw7_startmodetest.htm
tech.root: directdraw
ms.assetid: b669e3c7-b34b-4919-9a3e-0349288360ba
ms.date: 12/05/2018
ms.keywords: IDirectDraw7 interface [DirectDraw],StartModeTest method, IDirectDraw7.StartModeTest, IDirectDraw7::StartModeTest, StartModeTest, StartModeTest method [DirectDraw], StartModeTest method [DirectDraw],IDirectDraw7 interface, ddraw/IDirectDraw7::StartModeTest, directdraw.idirectdraw7_startmodetest
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectDraw7::StartModeTest
 - ddraw/IDirectDraw7::StartModeTest
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ddraw.dll
api_name:
 - IDirectDraw7.StartModeTest
---

# IDirectDraw7::StartModeTest


## -description

Initiates a test to update the system registry with refresh rate information for the current display adapter and monitor combination. A call to this method is typically followed by calls to <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-evaluatemode">IDirectDraw7::EvaluateMode</a> to pass or fail modes displayed by the test.

## -parameters

### -param unnamedParam1 [in]

An array of SIZE elements that describe, in terms of screen resolutions, the modes that should be tested.

### -param unnamedParam2 [in]

The number of elements in the array that the  <i>lpModesToTest</i> parameter specifies.

### -param unnamedParam3 [in]

Flags that specify options for starting a test. The only flag value that is currently valid is DDSMT_ISTESTREQUIRED. When this flag is specified, <b>StartModeTest</b> does not initiate a test, but instead returns a value that indicates whether it is possible or necessary to test the resolutions that the <i>lpModesToTest</i> and <i>dwNumEntries</i> parameters identify.

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

You can use the <b>StartModeTest</b> method together with the <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-evaluatemode">IDirectDraw7::EvaluateMode</a> method to determine the maximum refresh rate that an EDID monitor and display adapter combination can support for each screen resolution. The results of the testing are stored in the system registry and affect the operation of <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-enumdisplaymodes">IDirectDraw7::EnumDisplayModes</a> when that method is called with the DDEDM_REFRESHRATES flag set.



Specifically, a call to <b>StartModeTest</b> directs DirectDraw to establish a set of testable resolutions and to display a mode based on the first resolution in the set. Subsequent calls to <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-evaluatemode">IDirectDraw7::EvaluateMode</a> can be used to pass or fail each mode and to advance the test to the next display mode.



<b>StartModeTest</b> succeeds only with monitors that contain EDID data. If the monitor is not EDID-compliant, <b>StartModeTest</b> returns DDERR_TESTFINISHED without testing any modes. If the EDID table does not contain values higher than 60 Hz, no modes are tested. Refresh rates higher than 100 Hz are tested only if the EDID table contains values higher than 85 Hz.



If you call <b>StartModeTest</b> with an argument list of (NULL, 0, 0), <b>StartModeTest</b> clears existing refresh rate information from the registry.



The test does not guarantee to display only the resolutions in the array described by the <i>lpModesToTest</i> and <i>dwNumEntries</i> parameters. For example, the 640×480 resolution is used to obtain a maximum viewable refresh rate for the 320×200 resolution.





## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdraw7">IDirectDraw7</a>