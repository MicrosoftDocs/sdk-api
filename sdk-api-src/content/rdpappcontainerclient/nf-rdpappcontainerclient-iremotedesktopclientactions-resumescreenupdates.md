---
UID: NF:rdpappcontainerclient.IRemoteDesktopClientActions.ResumeScreenUpdates
title: IRemoteDesktopClientActions::ResumeScreenUpdates (rdpappcontainerclient.h)
description: Resumes screen updates being sent to the client.
helpviewer_keywords: ["IRemoteDesktopClientActions interface [Remote Desktop Services]","ResumeScreenUpdates method","IRemoteDesktopClientActions.ResumeScreenUpdates","IRemoteDesktopClientActions::ResumeScreenUpdates","ResumeScreenUpdates","ResumeScreenUpdates method [Remote Desktop Services]","ResumeScreenUpdates method [Remote Desktop Services]","IRemoteDesktopClientActions interface","rdpappcontainerclient/IRemoteDesktopClientActions::ResumeScreenUpdates","termserv.iremotedesktopclientactions_resumescreenupdates"]
old-location: termserv\iremotedesktopclientactions_resumescreenupdates.htm
tech.root: TermServ
ms.assetid: be11f1c8-eb55-4ed3-80ca-eda9ee21c92c
ms.date: 12/05/2018
ms.keywords: IRemoteDesktopClientActions interface [Remote Desktop Services],ResumeScreenUpdates method, IRemoteDesktopClientActions.ResumeScreenUpdates, IRemoteDesktopClientActions::ResumeScreenUpdates, ResumeScreenUpdates, ResumeScreenUpdates method [Remote Desktop Services], ResumeScreenUpdates method [Remote Desktop Services],IRemoteDesktopClientActions interface, rdpappcontainerclient/IRemoteDesktopClientActions::ResumeScreenUpdates, termserv.iremotedesktopclientactions_resumescreenupdates
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
 - IRemoteDesktopClientActions::ResumeScreenUpdates
 - rdpappcontainerclient/IRemoteDesktopClientActions::ResumeScreenUpdates
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
 - IRemoteDesktopClientActions.ResumeScreenUpdates
---

# IRemoteDesktopClientActions::ResumeScreenUpdates


## -description

Resumes screen updates being sent to the client.



Use the <a href="/windows/desktop/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclientactions-suspendscreenupdates">SuspendScreenUpdates</a> method to suspend screen updates.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclientactions">IRemoteDesktopClientActions</a>
