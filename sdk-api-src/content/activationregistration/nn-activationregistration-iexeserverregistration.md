---
UID: NN:activationregistration.IExeServerRegistration
title: IExeServerRegistration
author: windows-sdk-content
description: Represents a registered an out-of-process server.
old-location: winrt\iexeserverregistration.htm
tech.root: WinRT
ms.assetid: 9A96968D-B9BD-4C47-B626-69B6EA6AE7EA
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IExeServerRegistration, IExeServerRegistration interface [Windows Runtime], IExeServerRegistration interface [Windows Runtime],described, activationregistration/IExeServerRegistration, winrt.iexeserverregistration
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: activationregistration.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - activationregistration.h
api_name:
 - IExeServerRegistration
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IExeServerRegistration interface


## -description


Represents a registered an out-of-process server.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IExeServerRegistration</b> interface inherits from <a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a>. <b>IExeServerRegistration</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IExeServerRegistration</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DC0E3542-662F-43B8-968B-9F565D9D9278">get_AppUserModelId</a>
</td>
<td align="left" width="63%">
Gets the identifier for the app's user model.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2A4B80B9-3590-411C-8834-6850A44AF46C">get_CommandLine</a>
</td>
<td align="left" width="63%">
Gets the command line used to launch the out-of-process server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/69E8D576-B842-4CD4-8D93-87E4E08D11CA">get_ExePath</a>
</td>
<td align="left" width="63%">
Gets the file path to the out-of-process server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DA667D7C-323B-412D-AF9E-03402223292A">get_Identity</a>
</td>
<td align="left" width="63%">
Gets the identity of the out-of-process server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DF0A20D8-5028-4A7B-B8E6-CAF5C3716407">get_IdentityType</a>
</td>
<td align="left" width="63%">
Gets the activation type for the out-of-process server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/23618FBC-2404-4AB7-9842-7FD439F677B1">get_Instancing</a>
</td>
<td align="left" width="63%">
Gets the instancing behavior for the out-of-process server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/06267C33-11B4-4B55-8D2C-A20926EE89DF">get_Permissions</a>
</td>
<td align="left" width="63%">
Gets the permissions for the out-of-process server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CB7CAA65-4DA9-4948-AEB4-150A45629947">get_ServerName</a>
</td>
<td align="left" width="63%">
Gets the name of the current out-of-process server.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/1D8F7B12-2883-478D-B83D-84AC47D512E4">IExeServerActivatableClassRegistration</a>



<a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a>
 

 

