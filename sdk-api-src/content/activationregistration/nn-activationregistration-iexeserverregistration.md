---
UID: NN:activationregistration.IExeServerRegistration
title: IExeServerRegistration (activationregistration.h)
description: Represents a registered an out-of-process server.helpviewer_keywords: ["IExeServerRegistration","IExeServerRegistration interface [Windows Runtime]","IExeServerRegistration interface [Windows Runtime]","described","activationregistration/IExeServerRegistration","winrt.iexeserverregistration"]
old-location: winrt\iexeserverregistration.htm
tech.root: WinRT
ms.assetid: 9A96968D-B9BD-4C47-B626-69B6EA6AE7EA
ms.date: 12/05/2018
ms.keywords: IExeServerRegistration, IExeServerRegistration interface [Windows Runtime], IExeServerRegistration interface [Windows Runtime],described, activationregistration/IExeServerRegistration, winrt.iexeserverregistration
f1_keywords:
- activationregistration/IExeServerRegistration
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IExeServerRegistration interface


## -description


Represents a registered an out-of-process server.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IExeServerRegistration</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>. <b>IExeServerRegistration</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/activationregistration/nf-activationregistration-iexeserverregistration-get_appusermodelid">get_AppUserModelId</a>
</td>
<td align="left" width="63%">
Gets the identifier for the app's user model.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/activationregistration/nf-activationregistration-iexeserverregistration-get_commandline">get_CommandLine</a>
</td>
<td align="left" width="63%">
Gets the command line used to launch the out-of-process server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/activationregistration/nf-activationregistration-iexeserverregistration-get_exepath">get_ExePath</a>
</td>
<td align="left" width="63%">
Gets the file path to the out-of-process server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/activationregistration/nf-activationregistration-iexeserverregistration-get_identity">get_Identity</a>
</td>
<td align="left" width="63%">
Gets the identity of the out-of-process server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/activationregistration/nf-activationregistration-iexeserverregistration-get_identitytype">get_IdentityType</a>
</td>
<td align="left" width="63%">
Gets the activation type for the out-of-process server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/activationregistration/nf-activationregistration-iexeserverregistration-get_instancing">get_Instancing</a>
</td>
<td align="left" width="63%">
Gets the instancing behavior for the out-of-process server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/activationregistration/nf-activationregistration-iexeserverregistration-get_permissions">get_Permissions</a>
</td>
<td align="left" width="63%">
Gets the permissions for the out-of-process server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/activationregistration/nf-activationregistration-iexeserverregistration-get_servername">get_ServerName</a>
</td>
<td align="left" width="63%">
Gets the name of the current out-of-process server.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/activationregistration/nn-activationregistration-iexeserveractivatableclassregistration">IExeServerActivatableClassRegistration</a>



<a href="https://docs.microsoft.com/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>
 

 

