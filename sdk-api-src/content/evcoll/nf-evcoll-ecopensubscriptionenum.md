---
UID: NF:evcoll.EcOpenSubscriptionEnum
title: EcOpenSubscriptionEnum function (evcoll.h)
author: windows-sdk-content
description: Creates a subscription enumerator to enumerate all registered subscriptions on the local machine.
old-location: wec\ecopensubscriptionenum.htm
tech.root: WEC
ms.assetid: edbfabb0-6ad1-415a-a2ef-094b1d3bcccb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EcOpenSubscriptionEnum, EcOpenSubscriptionEnum function, evcoll/EcOpenSubscriptionEnum, wec.ecopensubscriptionenum, wes.ecopensubscriptionenum
ms.topic: function
f1_keywords: 
 - "evcoll/EcOpenSubscriptionEnum"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wecapi.dll
api_name:
 - EcOpenSubscriptionEnum
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EcOpenSubscriptionEnum function


## -description


The <b>EcOpenSubscriptionEnum</b> function is creates a subscription enumerator to enumerate all registered subscriptions on the local machine.


## -parameters




### -param Flags [in]

Reserved. Must be 0.


## -returns



If the function succeeds, it returns an handle (<a href="https://docs.microsoft.com/windows/desktop/WEC/windows-event-collector-data-types">EC_HANDLE</a>) to a new subscription enumerator object. Returns <b>NULL</b> otherwise, in which case use the <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function to obtain the error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WEC/windows-event-collector-functions">Windows Event Collector Functions</a>
 

 

