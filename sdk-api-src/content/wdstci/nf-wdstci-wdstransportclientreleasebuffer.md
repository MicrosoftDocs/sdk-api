---
UID: NF:wdstci.WdsTransportClientReleaseBuffer
title: WdsTransportClientReleaseBuffer function (wdstci.h)
description: Decrements the reference count on a buffer owned by the multicast client.
helpviewer_keywords: ["WdsTransportClientReleaseBuffer","WdsTransportClientReleaseBuffer function [Windows Deployment Services]","wds.wdstransportclientreleasebuffer","wdstci/WdsTransportClientReleaseBuffer"]
old-location: wds\wdstransportclientreleasebuffer.htm
tech.root: wds
ms.assetid: bf0dcb89-0bc2-4e93-94ce-5c50039ef22b
ms.date: 12/05/2018
ms.keywords: WdsTransportClientReleaseBuffer, WdsTransportClientReleaseBuffer function [Windows Deployment Services], wds.wdstransportclientreleasebuffer, wdstci/WdsTransportClientReleaseBuffer
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
 - WdsTransportClientReleaseBuffer
 - wdstci/WdsTransportClientReleaseBuffer
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
 - WdsTransportClientReleaseBuffer
---

# WdsTransportClientReleaseBuffer function


## -description

Decrements the reference count on a buffer owned by the multicast client.

## -parameters

### -param pvBuffer [in]

The buffer on which to decrement the reference count.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

