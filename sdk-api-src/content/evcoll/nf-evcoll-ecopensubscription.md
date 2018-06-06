---
UID: NF:evcoll.EcOpenSubscription
title: EcOpenSubscription function
author: windows-sdk-content
description: Opens an existing subscription or creates a new subscription.
old-location: wec\ecopensubscription.htm
old-project: WEC
ms.assetid: 3b4ef765-b557-4142-ba7d-e2556bd067ec
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: EcOpenSubscription, EcOpenSubscription function, evcoll/EcOpenSubscription, wec.ecopensubscription, wes.ecopensubscription
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
 - EcOpenSubscription
product: Windows
targetos: Windows
req.lib: Wecapi.lib
req.dll: Wecapi.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# EcOpenSubscription function


## -description


The <b>EcOpenSubscription</b> function is used to open an existing subscription or create a new subscription according to the flag value specified.


## -parameters




### -param SubscriptionName [in]

Specifies the name of the subscription. The value provided for this parameter should be unique within the computer's scope.


### -param AccessMask [in]

An access mask that specifies the desired access rights to the subscription. Use the <a href="https://msdn.microsoft.com/2ba862f9-6849-43b3-8914-e18ede1d63c0">EC_READ_ACCESS</a> or <a href="https://msdn.microsoft.com/2ba862f9-6849-43b3-8914-e18ede1d63c0">EC_WRITE_ACCESS</a> constants to specify the access rights. The function fails if the security descriptor of the subscription does not permit the requested access for the calling process.


### -param Flags [in]

A value specifying whether a new or existing subscription will be opened. Use the <b>EC_CREATE_NEW</b>, <b>EC_OPEN_ALWAYS</b>, or <b>EC_OPEN_EXISTING</b> constants.


## -returns



If the function succeeds, it returns an handle (<a href="https://msdn.microsoft.com/b78bdaf8-e034-40fe-acf8-632313e4fd94">EC_HANDLE</a>) to a new subscription object. Returns <b>NULL</b> otherwise, in which case use the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function to obtain the error code.




## -see-also




<a href="https://msdn.microsoft.com/48155df6-ba9c-4abe-ba84-6190cee95878">Windows Event Collector Functions</a>
 

 

