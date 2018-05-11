---
UID: NF:rdpappcontainerclient.IRemoteDesktopClientActions.GetSnapshot
title: IRemoteDesktopClientActions::GetSnapshot
author: windows-driver-content
description: Causes a snapshot of the Remote Desktop Protocol (RDP) app container client's in-session desktop to be taken.
old-location: termserv\iremotedesktopclientactions_getsnapshot.htm
old-project: TermServ
ms.assetid: c80fe6e3-6ca7-4595-aa0e-c1ed0f6632a5
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: GetSnapshot, GetSnapshot method [Remote Desktop Services], GetSnapshot method [Remote Desktop Services],IRemoteDesktopClientActions interface, IRemoteDesktopClientActions interface [Remote Desktop Services],GetSnapshot method, IRemoteDesktopClientActions.GetSnapshot, IRemoteDesktopClientActions::GetSnapshot, rdpappcontainerclient/IRemoteDesktopClientActions::GetSnapshot, termserv.iremotedesktopclientactions_getsnapshot
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: SnapshotFormatType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	MsTscAx.dll
api_name:
-	IRemoteDesktopClientActions.GetSnapshot
product: Windows
targetos: Windows
req.lib: 
req.dll: MsTscAx.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IRemoteDesktopClientActions::GetSnapshot


## -description



Causes a snapshot of the Remote Desktop Protocol (RDP) app container client's in-session desktop to be taken.




## -parameters




### -param snapshotEncoding [in]

Specifies the encoding type for the snapshot.


### -param snapshotFormat [in]

Specifies the data format type for the snapshot


### -param snapshotWidth [in]

The width, in pixels, of the snapshot.


### -param snapshotHeight [in]

The height, in pixels, of the snapshot.


### -param snapshotData [out, retval]

On return points to the snapshot.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/64b3683e-e577-48c1-a319-601e7944f68a">IRemoteDesktopClientActions</a>
 

 

