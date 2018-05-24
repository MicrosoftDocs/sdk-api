---
UID: NN:shldisp.IShellDispatch4
title: IShellDispatch4
author: windows-driver-content
description: Extends the IShellDispatch3 object.
old-location: shell\IShellDispatch4.htm
old-project: shell
ms.assetid: 4fe37e38-ee71-41f0-b620-35fdc18f9dbb
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IShellDispatch4, IShellDispatch4 object [Windows Shell], IShellDispatch4 object [Windows Shell],described, _shell_IShellDispatch4, shell.IShellDispatch4, shldisp/IShellDispatch4
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: shldisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.typenames: AUTOCOMPLETEOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shell32.dll
api_name:
-	IShellDispatch4
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 6.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellDispatch4 interface


## -description


Extends the <a href="https://msdn.microsoft.com/89d0aa4d-844d-497d-82bb-bcc2bcf9c78b">IShellDispatch3</a> object. In addition to the properties and methods supported by <b>IShellDispatch3</b>, <b>IShellDispatch4</b> supports four additional methods.

            
<div class="alert"><b>Note</b>  <b>IShellDispatch4</b> is implemented and accessed through the <a href="https://msdn.microsoft.com/library/windows/hardware/mt270130">Shell</a> object.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellDispatch4</b> object has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IShellDispatch4</b> object has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/490c3e18-b606-456a-9016-dc4f7bad2bc3">ExplorerPolicy</a>
</td>
<td align="left" width="63%">
Gets the value for a specified Internet Explorer policy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b9b1542c-8e25-4966-b3df-13bfbd9b28aa">GetSetting</a>
</td>
<td align="left" width="63%">
Retrieves a global Shell setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/60199e18-b8da-48a6-b316-e7f07ff44b78">ToggleDesktop</a>
</td>
<td align="left" width="63%">
Displays or hides the desktop.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/665c4644-7749-446e-8212-3ecc9901a035">WindowsSecurity</a>
</td>
<td align="left" width="63%">
Displays the <b>Windows Security</b> dialog box.

</td>
</tr>
</table> 


## -remarks



For a discussion of Windows services, see the <a href="https://msdn.microsoft.com/library/windows/hardware/dn926947">Services</a> documentation.




## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/9B429C03-7F80-45db-B8CD-58D19FAD2E61">IShellDispatch</a>



<a href="https://msdn.microsoft.com/74687929-0777-479b-9853-2b0cf4b6adc9">IShellDispatch2</a>



<a href="https://msdn.microsoft.com/89d0aa4d-844d-497d-82bb-bcc2bcf9c78b">IShellDispatch3</a>



<a href="https://msdn.microsoft.com/75fc151e-5b9e-476b-b4e5-b848917357a8">Shell Object</a>
 

 

