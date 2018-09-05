---
UID: NF:evcoll.EcOpenSubscriptionEnum
title: EcOpenSubscriptionEnum function
author: windows-sdk-content
description: Creates a subscription enumerator to enumerate all registered subscriptions on the local machine.
old-location: wec\ecopensubscriptionenum.htm
old-project: WEC
ms.assetid: edbfabb0-6ad1-415a-a2ef-094b1d3bcccb
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: EcOpenSubscriptionEnum, EcOpenSubscriptionEnum function, evcoll/EcOpenSubscriptionEnum, wec.ecopensubscriptionenum, wes.ecopensubscriptionenum
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: evcoll.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: EC_VARIANT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wecapi.dll
api_name:
 - EcOpenSubscriptionEnum
product: Windows
targetos: Windows
req.lib: Wecapi.lib
req.dll: Wecapi.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# EcOpenSubscriptionEnum function


## -description


The <b>EcOpenSubscriptionEnum</b> function is creates a subscription enumerator to enumerate all registered subscriptions on the local machine.


## -parameters




### -param Flags [in]

Reserved. Must be 0.


## -returns



If the function succeeds, it returns an handle (<a href="https://msdn.microsoft.com/b78bdaf8-e034-40fe-acf8-632313e4fd94">EC_HANDLE</a>) to a new subscription enumerator object. Returns <b>NULL</b> otherwise, in which case use the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function to obtain the error code.




## -see-also




<a href="https://msdn.microsoft.com/48155df6-ba9c-4abe-ba84-6190cee95878">Windows Event Collector Functions</a>
 

 

