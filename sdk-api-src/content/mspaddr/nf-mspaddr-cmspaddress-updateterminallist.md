---
UID: NF:mspaddr.CMSPAddress.UpdateTerminalList
title: CMSPAddress::UpdateTerminalList
author: windows-driver-content
description: The UpdateTerminalList method populates the MSP's list of static terminals.
old-location: tapi3\cmspaddress_updateterminallist.htm
old-project: Tapi
ms.assetid: f40964fe-21fe-4dad-8e56-71623ed2be1d
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: CMSPAddress interface [TAPI 2.2],UpdateTerminalList method, CMSPAddress.UpdateTerminalList, CMSPAddress::UpdateTerminalList, UpdateTerminalList, UpdateTerminalList method [TAPI 2.2], UpdateTerminalList method [TAPI 2.2],CMSPAddress interface, _tapi3_cmspaddress_updateterminallist, mspaddr/CMSPAddress::UpdateTerminalList, tapi3.cmspaddress_updateterminallist
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mspaddr.h
req.include-header: 
req.target-type: Windows
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
req.typenames: MSP_EVENT_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mspaddr.h
api_name:
-	CMSPAddress.UpdateTerminalList
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# CMSPAddress::UpdateTerminalList


## -description


The 
<b>UpdateTerminalList</b> method populates the MSP's list of static terminals. It assumes that we have no static terminals available and it is always called in situations where this is true. This method uses DirectShow's "devenum" component and a static list of categories to discover monikers for static terminals. It uses the static 
<a href="https://msdn.microsoft.com/2a2a037a-753c-4dd4-b6ce-10b69f2e2421">CreateTerminal</a> methods on each type of terminal (see below) to actually create the terminals, possibly failing if the moniker in question is not acceptable (see below). For each successfully created terminal, it adds the terminal to the address' list. When this process is complete, devenum is released. An MSP that uses different static terminals than the ones created or that needs to use additional static terminals must override this method. The categories currently used here are CLSID_CWaveInClassManager, CLSID_CWaveOutClassManager, and CLSID_CVidCapClassManager. The method does not use categories that correspond to media types that the derived MSP does not support (this is checked automatically in the base class).


## -parameters






## -see-also




<a href="https://msdn.microsoft.com/864bf814-43dd-4d2b-a5a7-fff12520accb">CMSPAddress</a>
 

 

