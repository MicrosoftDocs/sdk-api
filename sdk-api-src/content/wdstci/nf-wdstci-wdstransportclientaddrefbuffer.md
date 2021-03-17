---
UID: NF:wdstci.WdsTransportClientAddRefBuffer
title: WdsTransportClientAddRefBuffer function (wdstci.h)
description: Increments the reference count on a buffer owned by the multicast client.
helpviewer_keywords: ["WdsTransportClientAddRefBuffer","WdsTransportClientAddRefBuffer function [Windows Deployment Services]","wds.wdstransportclientaddrefbuffer","wdstci/WdsTransportClientAddRefBuffer"]
old-location: wds\wdstransportclientaddrefbuffer.htm
tech.root: wds
ms.assetid: 941cac20-cca9-4351-8dee-f3910062c6b4
ms.date: 12/05/2018
ms.keywords: WdsTransportClientAddRefBuffer, WdsTransportClientAddRefBuffer function [Windows Deployment Services], wds.wdstransportclientaddrefbuffer, wdstci/WdsTransportClientAddRefBuffer
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
 - WdsTransportClientAddRefBuffer
 - wdstci/WdsTransportClientAddRefBuffer
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
 - WdsTransportClientAddRefBuffer
---

# WdsTransportClientAddRefBuffer function


## -description

Increments the reference count on a buffer owned by the multicast client.

## -parameters

### -param pvBuffer [in]

The buffer on which to increment the reference count.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

