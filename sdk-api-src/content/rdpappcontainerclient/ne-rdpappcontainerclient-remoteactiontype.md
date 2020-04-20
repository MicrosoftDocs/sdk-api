---
UID: NE:rdpappcontainerclient.__MIDL_IRemoteDesktopClientActions_0001
title: RemoteActionType (rdpappcontainerclient.h)
description: The action to send to the remote session.helpviewer_keywords: ["RemoteActionAppSwitch","RemoteActionAppbar","RemoteActionCharms","RemoteActionSnap","RemoteActionStartScreen","RemoteActionType","RemoteActionType enumeration [Remote Desktop Services]","rdpappcontainerclient/RemoteActionAppSwitch","rdpappcontainerclient/RemoteActionAppbar","rdpappcontainerclient/RemoteActionCharms","rdpappcontainerclient/RemoteActionSnap","rdpappcontainerclient/RemoteActionStartScreen","rdpappcontainerclient/RemoteActionType","termserv.remoteactiontype"]
old-location: termserv\remoteactiontype.htm
tech.root: TermServ
ms.assetid: 27E6FB88-54A6-4D0B-B0D0-A46A96299DD1
ms.date: 12/05/2018
ms.keywords: RemoteActionAppSwitch, RemoteActionAppbar, RemoteActionCharms, RemoteActionSnap, RemoteActionStartScreen, RemoteActionType, RemoteActionType enumeration [Remote Desktop Services], rdpappcontainerclient/RemoteActionAppSwitch, rdpappcontainerclient/RemoteActionAppbar, rdpappcontainerclient/RemoteActionCharms, rdpappcontainerclient/RemoteActionSnap, rdpappcontainerclient/RemoteActionStartScreen, rdpappcontainerclient/RemoteActionType, termserv.remoteactiontype
f1_keywords:
- rdpappcontainerclient/RemoteActionType
dev_langs:
- c++
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
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- LibDef
api_location:
- MsTscAx.dll
api_name:
- RemoteActionType
targetos: Windows
req.typenames: RemoteActionType
req.redist: 
ms.custom: 19H1
---

# RemoteActionType enumeration


## -description


The action to send to the remote session.



## -enum-fields




### -field RemoteActionCharms

Displays the charms in the remote session.


### -field RemoteActionAppbar

Displays the app bar in the remote session.


### -field RemoteActionSnap

Docks the application in the remote session.


### -field RemoteActionStartScreen

Causes the start screen to be displayed in the remote session.


### -field RemoteActionAppSwitch

Causes the application switch window to be displayed in the remote session. This is the same as the user pressing Alt+Tab.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclientactions-executeremoteaction">ExecuteRemoteAction</a>
 

 

