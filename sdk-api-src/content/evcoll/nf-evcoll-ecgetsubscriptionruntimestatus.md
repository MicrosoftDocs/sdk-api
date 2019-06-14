---
UID: NF:evcoll.EcGetSubscriptionRunTimeStatus
title: EcGetSubscriptionRunTimeStatus function (evcoll.h)
author: windows-sdk-content
description: Retrieves the run time status information for an event source of a subscription or the subscription itself.
old-location: wec\ecgetsubscriptionruntimestatus.htm
tech.root: WEC
ms.assetid: 17d9d264-5ae3-4e31-869c-ada0c6c5c53b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EcGetSubscriptionRunTimeStatus, EcGetSubscriptionRunTimeStatus function, evcoll/EcGetSubscriptionRunTimeStatus, wec.ecgetsubscriptionruntimestatus, wes.ecgetsubscriptionruntimestatus
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
 - EcGetSubscriptionRunTimeStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EcGetSubscriptionRunTimeStatus function


## -description


The <b>EcGetSubscriptionRunTimeStatus</b> function retrieves the run time status information for an event source of a subscription or the subscription itself. The subscription is specified by its name. If the event source is <b>NULL</b>, then the status for the overall subscription is retrieved.


## -parameters




### -param SubscriptionName [in]

The name of the subscription to get the run time status information from.


### -param StatusInfoId [in]

An identifier that specifies which run time status information to get from the subscription. Specify a value from the <a href="https://docs.microsoft.com/windows/desktop/api/evcoll/ne-evcoll-_ec_subscription_runtime_status_info_id">EC_SUBSCRIPTION_RUNTIME_STATUS_INFO_ID</a> enumeration. The <b>EcSubscriptionRunTimeStatusEventSources</b> value can be used to obtain the list of event sources associated with a subscription.


### -param EventSourceName [in]

The name of the event source to get the status from. Each subscription can have multiple event sources.


### -param Flags [in]

Reserved. Must be <b>NULL</b>.


### -param StatusValueBufferSize [in]

The size of the user-supplied buffer that will hold the run time status information.


### -param StatusValueBuffer [in]

The user-supplied buffer that will hold the run time status information. The buffer will hold the appropriate value depending on the <a href="https://docs.microsoft.com/windows/desktop/api/evcoll/ne-evcoll-_ec_subscription_runtime_status_info_id">EC_SUBSCRIPTION_RUNTIME_STATUS_INFO_ID</a> value passed into the <i>StatusInfoId</i> parameter.


### -param StatusValueBufferUsed [out]

The size of the user supplied buffer that is used by the function on successful return, or the size that is necessary to store the property value when function fails with <b>ERROR_INSUFFICIENT_BUFFER</b>.


## -returns



This function returns BOOL.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WEC/windows-event-collector-functions">Windows Event Collector Functions</a>
 

 

