---
UID: NN:shldisp.IShellDispatch2
title: IShellDispatch2
author: windows-sdk-content
description: Extends the IShellDispatch object with a variety of new functionality.
old-location: shell\IShellDispatch2_Object.htm
old-project: shell
ms.assetid: 74687929-0777-479b-9853-2b0cf4b6adc9
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IShellDispatch2, IShellDispatch2 object [Windows Shell], IShellDispatch2 object [Windows Shell],described, _win32_IShellDispatch2_Object, shell.IShellDispatch2_Object, shldisp/IShellDispatch2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shldisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shldisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: AUTOCOMPLETEOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellDispatch2
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellDispatch2 interface


## -description


Extends the <a href="https://msdn.microsoft.com/9B429C03-7F80-45db-B8CD-58D19FAD2E61">IShellDispatch</a> object with a variety of new functionality.
        
            
<div class="alert"><b>Note</b>  <b>IShellDispatch2</b> is implemented and accessed through the <a href="https://msdn.microsoft.com/library/windows/hardware/mt270130">Shell</a> object.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellDispatch2</b> object has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IShellDispatch2</b> object has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cbb54ae9-02e6-4243-a782-e9f125c21c0d">CanStartStopService</a>
</td>
<td align="left" width="63%">
Determines if the current user can start and stop the named service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a3d1e810-f0cf-48ec-93da-5cc01117c5d4">FindPrinter</a>
</td>
<td align="left" width="63%">
Displays the <b>Find Printer</b> dialog box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/57c066e3-080f-4ecc-b56e-877f0569e901">GetSystemInformation</a>
</td>
<td align="left" width="63%">
Retrieves system information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/04275c5f-c3ed-4962-882f-2cce0258a9f4">IsRestricted</a>
</td>
<td align="left" width="63%">
Retrieves a group's restriction setting from the registry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/91f3fba1-7aa5-423a-bc37-49db230c79db">IsServiceRunning</a>
</td>
<td align="left" width="63%">
Returns a value that indicates whether a particular service is running.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3af57cdc-f449-433d-a9e1-119038045e4c">ServiceStart</a>
</td>
<td align="left" width="63%">
Starts a named service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f4cd0e2c-4ecc-4e9f-a0b5-d2a8a739f0e2">ServiceStop</a>
</td>
<td align="left" width="63%">
Stops a named service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a55e804c-ed7c-4b22-b86f-8e5653976654">ShellExecute</a>
</td>
<td align="left" width="63%">
Performs a specified operation on a specified file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5776370c-3bbf-449b-a8fe-2dbc7d89dd25">ShowBrowserBar</a>
</td>
<td align="left" width="63%">
Displays a browser bar.

</td>
</tr>
</table> 


## -remarks



For a discussion of Windows services, see the <a href="https://msdn.microsoft.com/library/windows/hardware/dn926947">Services</a> documentation.




## -see-also




<a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/9B429C03-7F80-45db-B8CD-58D19FAD2E61">IShellDispatch</a>



<a href="https://msdn.microsoft.com/75fc151e-5b9e-476b-b4e5-b848917357a8">Shell Object</a>
 

 

