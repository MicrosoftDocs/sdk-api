---
UID: NN:shobjidl_core.ICreateProcessInputs
title: ICreateProcessInputs (shobjidl_core.h)
author: windows-sdk-content
description: Used by the ICreatingProcess interface to alter some parameters of the process that is being created.
old-location: shell\icreateprocessinputs.htm
tech.root: shell
ms.assetid: 2C1756A3-FF40-4FBF-860D-06BB415DB695
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICreateProcessInputs, ICreateProcessInputs interface [Windows Shell], ICreateProcessInputs interface [Windows Shell],described, shell.icreateprocessinputs, shobjidl_core/ICreateProcessInputs
ms.topic: interface
f1_keywords: 
 - "shobjidl_core/ICreateProcessInputs"
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - ICreateProcessInputs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICreateProcessInputs interface


## -description


Used by the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icreatingprocess">ICreatingProcess</a> interface to alter some parameters of the process that is being created.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICreateProcessInputs</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICreateProcessInputs</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICreateProcessInputs</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icreateprocessinputs-addcreateflags">AddCreateFlags</a>
</td>
<td align="left" width="63%">
 Set additional flags that will be included in the call to <a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icreateprocessinputs-addstartupflags">AddStartupFlags</a>
</td>
<td align="left" width="63%">
 Additional flags that will be included in the <a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/ns-processthreadsapi-_startupinfoa">STARTUPINFO</a> structure passed to <a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icreateprocessinputs-getcreateflags">GetCreateFlags</a>
</td>
<td align="left" width="63%">
Gets the additional flags that will be passed to <a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icreateprocessinputs-setcreateflags">SetCreateFlags</a>
</td>
<td align="left" width="63%">
 Set the flags that will be included in the call to <a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icreateprocessinputs-setenvironmentvariable">SetEnvironmentVariable</a>
</td>
<td align="left" width="63%">
Sets a variable in the environment of the created process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icreateprocessinputs-sethotkey">SetHotKey</a>
</td>
<td align="left" width="63%">
Sets the hot key for the application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icreateprocessinputs-settitle">SetTitle</a>
</td>
<td align="left" width="63%">
 Sets the title that will be passed <a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>.

</td>
</tr>
</table> 


## -remarks



Applications do not implement this interface.

A pointer to this interface is passed to <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icreatingprocess-oncreating">ICreatingProcess::OnCreating</a>.



