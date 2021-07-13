---
UID: NF:mspaddr.CMSPAddress.UpdateTerminalList
title: CMSPAddress::UpdateTerminalList (mspaddr.h)
description: The UpdateTerminalList method populates the MSP's list of static terminals.
helpviewer_keywords: ["CMSPAddress interface [TAPI 2.2]","UpdateTerminalList method","CMSPAddress.UpdateTerminalList","CMSPAddress::UpdateTerminalList","UpdateTerminalList","UpdateTerminalList method [TAPI 2.2]","UpdateTerminalList method [TAPI 2.2]","CMSPAddress interface","_tapi3_cmspaddress_updateterminallist","mspaddr/CMSPAddress::UpdateTerminalList","tapi3.cmspaddress_updateterminallist"]
old-location: tapi3\cmspaddress_updateterminallist.htm
tech.root: tapi3
ms.assetid: f40964fe-21fe-4dad-8e56-71623ed2be1d
ms.date: 12/05/2018
ms.keywords: CMSPAddress interface [TAPI 2.2],UpdateTerminalList method, CMSPAddress.UpdateTerminalList, CMSPAddress::UpdateTerminalList, UpdateTerminalList, UpdateTerminalList method [TAPI 2.2], UpdateTerminalList method [TAPI 2.2],CMSPAddress interface, _tapi3_cmspaddress_updateterminallist, mspaddr/CMSPAddress::UpdateTerminalList, tapi3.cmspaddress_updateterminallist
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CMSPAddress::UpdateTerminalList
 - mspaddr/CMSPAddress::UpdateTerminalList
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mspaddr.h
api_name:
 - CMSPAddress.UpdateTerminalList
---

# CMSPAddress::UpdateTerminalList


## -description

The 
<b>UpdateTerminalList</b> method populates the MSP's list of static terminals. It assumes that we have no static terminals available and it is always called in situations where this is true. This method uses DirectShow's "devenum" component and a static list of categories to discover monikers for static terminals. It uses the static 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal">CreateTerminal</a> methods on each type of terminal (see below) to actually create the terminals, possibly failing if the moniker in question is not acceptable (see below). For each successfully created terminal, it adds the terminal to the address' list. When this process is complete, devenum is released. An MSP that uses different static terminals than the ones created or that needs to use additional static terminals must override this method. The categories currently used here are CLSID_CWaveInClassManager, CLSID_CWaveOutClassManager, and CLSID_CVidCapClassManager. The method does not use categories that correspond to media types that the derived MSP does not support (this is checked automatically in the base class).



## -see-also

<a href="/windows/desktop/api/mspaddr/nl-mspaddr-cmspaddress">CMSPAddress</a>
