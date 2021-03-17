---
UID: NF:wdstpdi.WdsTransportServerCompleteRead
title: WdsTransportServerCompleteRead function (wdstpdi.h)
description: Provides status of read operation.
helpviewer_keywords: ["WdsTransportServerCompleteRead","WdsTransportServerCompleteRead function [Windows Deployment Services]","wds.wdstransportservercompleteread","wdstpdi/WdsTransportServerCompleteRead"]
old-location: wds\wdstransportservercompleteread.htm
tech.root: wds
ms.assetid: 0f98305d-4173-4d6f-9132-f1fcc12364ed
ms.date: 12/05/2018
ms.keywords: WdsTransportServerCompleteRead, WdsTransportServerCompleteRead function [Windows Deployment Services], wds.wdstransportservercompleteread, wdstpdi/WdsTransportServerCompleteRead
req.header: wdstpdi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wdsmc.lib
req.dll: Wdsmc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WdsTransportServerCompleteRead
 - wdstpdi/WdsTransportServerCompleteRead
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wdsmc.dll
api_name:
 - WdsTransportServerCompleteRead
---

# WdsTransportServerCompleteRead function


## -description

Provides status of read operation.

## -parameters

### -param hProvider [in]

Handle to the provider. This handle was given to the provider in the <a href="/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize">WdsTransportProviderInitialize</a> function.

### -param ulBytesRead [in]

The number of bytes read.

### -param pvUserData [in]

User data specified by <a href="/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderreadcontent">WdsTransportProviderReadContent</a>.

### -param hReadResult [in]

The status of this read operation.

## -returns

If the function succeeds, the return is <b>S_OK</b>.