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
f1_keywords: ["rdpappcontainerclient/IRemoteDesktopClientActions"]
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
ms.custom: 19H1
---

# IRemoteDesktopClientActions interface


## -description



Provides the methods used to interact with the Remote Desktop Protocol (RDP) app container client control.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRemoteDesktopClientActions</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IRemoteDesktopClientActions</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclientactions-executeremoteaction">ExecuteRemoteAction</a>
</td>
<td align="left" width="63%">
Causes an action to be performed in the remote session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclientactions-getsnapshot">GetSnapshot</a>
</td>
<td align="left" width="63%">
Causes a snapshot of the Remote Desktop Protocol (RDP) app container client's in-session desktop to be taken.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclientactions-resumescreenupdates">ResumeScreenUpdates</a>
</td>
<td align="left" width="63%">
Resumes screen updates being sent to the client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclientactions-suspendscreenupdates">SuspendScreenUpdates</a>
</td>
<td align="left" width="63%">
Suspends screen updates being sent to the client.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/TermServ/remote-desktop-activex-control-reference">Remote Desktop ActiveX control reference</a>
 

 

