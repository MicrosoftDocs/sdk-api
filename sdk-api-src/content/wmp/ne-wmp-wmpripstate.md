---
UID: NE:wmp.WMPRipState
title: WMPRipState
author: windows-driver-content
description: The WMPRipState enumeration type defines the possible operational states of Windows Media Player as it rips a CD.
old-location: wmp\wmpripstate.htm
old-project: WMP
ms.assetid: bd62cae1-3f63-4355-afc7-e429a444189d
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: WMPRipState, WMPRipState enumeration [Windows Media Player], wmp.wmpripstate, wmp/WMPRipState, wmp/wmprsRipping, wmp/wmprsStopped, wmp/wmprsUnknown, wmprsRipping, wmprsStopped, wmprsUnknown
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11.
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
req.typenames: WMPRipState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	wmp.h
api_name:
-	WMPRipState
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WMPRipState enumeration


## -description



The <b>WMPRipState</b> enumeration type defines the possible operational states of Windows Media Player as it rips a CD.




## -enum-fields




### -field wmprsUnknown

Not a valid state.


### -field wmprsRipping

Windows Media Player is ripping.


### -field wmprsStopped

The ripping operation is stopped.


## -remarks




          Windows Media Player 10 Mobile: This enumeration is not supported.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545452">Enumeration Types</a>



<a href="https://msdn.microsoft.com/c3e2db46-bef0-4c79-91b5-97ca5a86c6ba">IWMPCdromRip Interface</a>
 

 

