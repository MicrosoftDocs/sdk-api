---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

