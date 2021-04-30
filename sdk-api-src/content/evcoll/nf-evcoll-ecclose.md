---
UID: NF:evcoll.EcClose
title: EcClose function (evcoll.h)
description: Closes a handle received from other Event Collector functions.
helpviewer_keywords: ["EcClose","EcClose function","evcoll/EcClose","wec.ecclose","wes.ecclose"]
old-location: wec\ecclose.htm
tech.root: WEC
ms.assetid: a2dc71e3-7580-4484-9a08-4e3ee2139921
ms.date: 12/05/2018
ms.keywords: EcClose, EcClose function, evcoll/EcClose, wec.ecclose, wes.ecclose
req.header: evcoll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wecapi.lib
req.dll: Wecapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EcClose
 - evcoll/EcClose
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wecapi.dll
api_name:
 - EcClose
---

# EcClose function


## -description

The <b>EcClose</b> function closes a handle received from other Event Collector functions. Any handle returned by an event collector management API call must be closed using this call when the user is finished with the handle. The handle becomes invalid when this function is successfully called.

## -parameters

### -param Object [in]

A valid open handle returned from an event collector management API call.

## -returns

This function returns BOOL.

## -see-also

<a href="/windows/desktop/WEC/windows-event-collector-functions">Windows Event Collector Functions</a>