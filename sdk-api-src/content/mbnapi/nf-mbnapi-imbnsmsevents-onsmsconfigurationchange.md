---
UID: NF:mbnapi.IMbnSmsEvents.OnSmsConfigurationChange
title: IMbnSmsEvents::OnSmsConfigurationChange (mbnapi.h)
author: windows-sdk-content
description: Notification method that indicates that SMS configuration has changed or is available.
old-location: mbn\imbnsmsevents_onsmsconfigurationchange.htm
tech.root: mbn
ms.assetid: d6990732-60ef-43e5-b35c-9a3f0324d580
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMbnSmsEvents interface [Microsoft Broadband Networks],OnSmsConfigurationChange method, IMbnSmsEvents.OnSmsConfigurationChange, IMbnSmsEvents::OnSmsConfigurationChange, OnSmsConfigurationChange, OnSmsConfigurationChange method [Microsoft Broadband Networks], OnSmsConfigurationChange method [Microsoft Broadband Networks],IMbnSmsEvents interface, mbn.imbnsmsevents_onsmsconfigurationchange, mbnapi/IMbnSmsEvents::OnSmsConfigurationChange
ms.topic: method
f1_keywords: 
 - "mbnapi/IMbnSmsEvents.OnSmsConfigurationChange"
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnSmsEvents.OnSmsConfigurationChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMbnSmsEvents::OnSmsConfigurationChange


## -description


Notification method that indicates that SMS configuration has changed or is available.


## -parameters




### -param sms [in]

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbnsms">IMbnSms</a> interface representing the Mobile Broadband device for which the SMS configuration is now available.


## -returns



This method must return <b>S_OK</b>.




## -remarks



An application can use the <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbnsms">IMbnSms</a> to get the new configuration details.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbnsmsevents">IMbnSmsEvents</a>
 

 

