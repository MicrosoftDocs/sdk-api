---
UID: NF:wdstci.WdsTransportClientInitialize
title: WdsTransportClientInitialize function (wdstci.h)
description: Initializes the Multicast Client.
helpviewer_keywords: ["WdsTransportClientInitialize","WdsTransportClientInitialize function [Windows Deployment Services]","wds.wdstransportclientinitialize","wdstci/WdsTransportClientInitialize"]
old-location: wds\wdstransportclientinitialize.htm
tech.root: wds
ms.assetid: 6494a155-61de-40bd-a29a-79134da96bbe
ms.date: 12/05/2018
ms.keywords: WdsTransportClientInitialize, WdsTransportClientInitialize function [Windows Deployment Services], wds.wdstransportclientinitialize, wdstci/WdsTransportClientInitialize
req.header: wdstci.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wdstptc.lib
req.dll: Wdstptc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WdsTransportClientInitialize
 - wdstci/WdsTransportClientInitialize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wdstptc.dll
api_name:
 - WdsTransportClientInitialize
---

# WdsTransportClientInitialize function


## -description

Initializes the Multicast Client. This function should be called before any other function is called in the multicast client.



## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

