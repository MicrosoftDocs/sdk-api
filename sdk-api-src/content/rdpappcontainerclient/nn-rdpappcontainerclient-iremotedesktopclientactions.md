---
UID: NN:rdpappcontainerclient.IRemoteDesktopClientActions
title: IRemoteDesktopClientActions (rdpappcontainerclient.h)
author: windows-sdk-content
description: Provides the methods used to interact with the Remote Desktop Protocol (RDP) app container client control.
old-location: termserv\iremotedesktopclientactions.htm
tech.root: TermServ
ms.assetid: 64b3683e-e577-48c1-a319-601e7944f68a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IRemoteDesktopClientActions, IRemoteDesktopClientActions interface [Remote Desktop Services], IRemoteDesktopClientActions interface [Remote Desktop Services],described, rdpappcontainerclient/IRemoteDesktopClientActions, termserv.iremotedesktopclientactions
ms.topic: interface
req.header: rdpappcontainerclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: MsTscAx.dll
req.lib: 
req.dll: MsTscAx.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsTscAx.dll
api_name:
 - IRemoteDesktopClientActions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRemoteDesktopClientActions interface


## -description



Provides the methods used to interact with the Remote Desktop Protocol (RDP) app container client control.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRemoteDesktopClientActions</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IRemoteDesktopClientActions</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRemoteDesktopClientActions</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/944fbfe4-b033-471b-9a28-87349382d37a">ExecuteRemoteAction</a>
</td>
<td align="left" width="63%">
Causes an action to be performed in the remote session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c80fe6e3-6ca7-4595-aa0e-c1ed0f6632a5">GetSnapshot</a>
</td>
<td align="left" width="63%">
Causes a snapshot of the Remote Desktop Protocol (RDP) app container client's in-session desktop to be taken.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/be11f1c8-eb55-4ed3-80ca-eda9ee21c92c">ResumeScreenUpdates</a>
</td>
<td align="left" width="63%">
Resumes screen updates being sent to the client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0161ee5f-5e67-4bc9-b822-800c2b23ec44">SuspendScreenUpdates</a>
</td>
<td align="left" width="63%">
Suspends screen updates being sent to the client.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/EAF75483-90A4-4BB1-82A5-EFBB2219A55B">Remote Desktop ActiveX control reference</a>
 

 

