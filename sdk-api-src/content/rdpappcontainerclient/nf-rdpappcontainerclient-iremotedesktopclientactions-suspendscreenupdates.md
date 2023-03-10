---
UID: NF:rdpappcontainerclient.IRemoteDesktopClientActions.SuspendScreenUpdates
title: IRemoteDesktopClientActions::SuspendScreenUpdates (rdpappcontainerclient.h)
description: Suspends screen updates being sent to the client.
helpviewer_keywords: ["IRemoteDesktopClientActions interface [Remote Desktop Services]","SuspendScreenUpdates method","IRemoteDesktopClientActions.SuspendScreenUpdates","IRemoteDesktopClientActions::SuspendScreenUpdates","SuspendScreenUpdates","SuspendScreenUpdates method [Remote Desktop Services]","SuspendScreenUpdates method [Remote Desktop Services]","IRemoteDesktopClientActions interface","rdpappcontainerclient/IRemoteDesktopClientActions::SuspendScreenUpdates","termserv.iremotedesktopclientactions_suspendscreenupdates"]
old-location: termserv\iremotedesktopclientactions_suspendscreenupdates.htm
tech.root: TermServ
ms.assetid: 0161ee5f-5e67-4bc9-b822-800c2b23ec44
ms.date: 12/05/2018
ms.keywords: IRemoteDesktopClientActions interface [Remote Desktop Services],SuspendScreenUpdates method, IRemoteDesktopClientActions.SuspendScreenUpdates, IRemoteDesktopClientActions::SuspendScreenUpdates, SuspendScreenUpdates, SuspendScreenUpdates method [Remote Desktop Services], SuspendScreenUpdates method [Remote Desktop Services],IRemoteDesktopClientActions interface, rdpappcontainerclient/IRemoteDesktopClientActions::SuspendScreenUpdates, termserv.iremotedesktopclientactions_suspendscreenupdates
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRemoteDesktopClientActions::SuspendScreenUpdates
 - rdpappcontainerclient/IRemoteDesktopClientActions::SuspendScreenUpdates
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsTscAx.dll
api_name:
 - IRemoteDesktopClientActions.SuspendScreenUpdates
---

# IRemoteDesktopClientActions::SuspendScreenUpdates


## -description

Suspends screen updates being sent to the client.



Use the <a href="/windows/desktop/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclientactions-resumescreenupdates">ResumeScreenUpdates</a> method to resume screen updates.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclientactions">IRemoteDesktopClientActions</a>
