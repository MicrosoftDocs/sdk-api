---
UID: NF:winddi.DrvResetPDEV
title: DrvResetPDEV function
author: windows-sdk-content
description: The DrvResetPDEV function allows a graphics driver to transfer the state of the driver from an old PDEV structure to a new PDEV structure when a Win32 application calls ResetDC.
old-location: display\drvresetpdev.htm
old-project: display
ms.assetid: 8e530874-7774-4f8f-852c-001b2ce4a707
ms.author: windowssdkdev
ms.date: 06/26/2018
ms.keywords: DrvResetPDEV, DrvResetPDEV function [Display Devices], ddifncs_839f09e0-67dc-4c1f-a17b-dd0fd5316258.xml, display.drvresetpdev, winddi/DrvResetPDEV
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
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
 - DrvResetPDEV
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# DrvResetPDEV function


## -description


The <b>DrvResetPDEV</b> function allows a graphics driver to transfer the state of the driver from an old <a href="https://msdn.microsoft.com/139a10e9-203b-499b-9291-8537eae9189c">PDEV</a> structure to a new PDEV structure when a Win32 application calls <a href="https://msdn.microsoft.com/3f77db51-90d1-4a87-812b-1e129ae8fde9">ResetDC</a>.

## -parameters




### -param dhpdevOld

Caller-supplied handle to the original device PDEV structure. This handle was previously provided by the driver as a return value for <a href="https://msdn.microsoft.com/library/windows/hardware/ff556211">DrvEnablePDEV</a>.


### -param dhpdevNew

Caller-supplied handle to the new PDEV structure.


## -returns



This return value is <b>TRUE</b> if the function is successful. Otherwise it is <b>FALSE</b>, and an error code is logged.




## -remarks



A graphics driver's <b>DrvResetPDEV</b> function should be used for modifying the contents of a new PDEV structure, based on the contents of the old (currently in use) PDEV structure.

OpenGL display drivers that need to know about mode changes should implement <b>DrvResetPDEV</b>. Otherwise, all other display drivers typically do not need to implement this function.

<h3><a id="Note__The_following_information_pertains_to_printer_graphics_DLLs."></a><a id="note__the_following_information_pertains_to_printer_graphics_dlls."></a><a id="NOTE__THE_FOLLOWING_INFORMATION_PERTAINS_TO_PRINTER_GRAPHICS_DLLS."></a>Note  The following information pertains to printer graphics DLLs.</h3>
The function is called as a result of an application's call to the Win32 <a href="https://msdn.microsoft.com/3f77db51-90d1-4a87-812b-1e129ae8fde9">ResetDC</a> function, which in turn causes GDI to call the driver's <a href="https://msdn.microsoft.com/library/windows/hardware/ff556211">DrvEnablePDEV</a> to obtain a new PDEV structure. Because the driver can modify a PDEV structure's contents during the rendering of a print job, the <b>DrvResetPDEV</b> function allows the driver to transfer these modifications from the old PDEV structure to the new one.

Examples of the types of information that a printer graphics DLL might want to add to the new PDEV structure are pointers to cached font files, or flags indicating whether page initialization should (or should not) take place the next time <a href="https://msdn.microsoft.com/library/windows/hardware/ff556296">DrvStartDoc</a> or <a href="https://msdn.microsoft.com/library/windows/hardware/ff556298">DrvStartPage</a> is called. 

If <a href="https://msdn.microsoft.com/3f77db51-90d1-4a87-812b-1e129ae8fde9">ResetDC</a> is called during the rendering of a print document, the printer graphics DLL receives the following sequence of calls:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>    dhpdevNew = DrvEnablePDEV();
    DrvResetPDEV(dhpdevOld, dhpdevNew);
    DrvDisableSurface(dhpdevOld);
    DrvDisablePDEV(dhpdevOld);
    DrvEnableSurface(dhpdevNew);
    DrvStartDoc(dhpdevNew);</pre>
</td>
</tr>
</table></span></div>
If  <a href="https://msdn.microsoft.com/3f77db51-90d1-4a87-812b-1e129ae8fde9">ResetDC</a> is called between documents there is no surface associated with the PDEV, so only the following sequence of calls is made:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>    dhpdevNew = DrvEnablePDEV();
    DrvResetPDEV(dhpdevOld,dhpdevNew);
    DrvDisablePDEV(dhpdevOld);</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556198">DrvDisablePDEV</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556200">DrvDisableSurface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556211">DrvEnablePDEV</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556214">DrvEnableSurface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556296">DrvStartDoc</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556298">DrvStartPage</a>
 

 

