---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# FAX_SCHEDULE_TYPE_ENUM enumeration


## -description


The <b>FAX_SCHEDULE_TYPE_ENUM</b> enumeration defines the types of scheduling for outbound faxes.


## -enum-fields




### -field fstNOW

Send the fax as soon as a device is available.


### -field fstSPECIFIC_TIME

Send the fax no sooner than the specified time. The actual time that the fax will be sent depends on device availability and fax priority.


### -field fstDISCOUNT_PERIOD

Send the fax during the discount rate period.


## -see-also




<a href="https://msdn.microsoft.com/1c8f5adf-9c94-4c4b-9a9a-e8377682f6f9">IFaxDocument::get_ScheduleTime</a>



<a href="https://msdn.microsoft.com/cbcfcdb1-de89-4e74-8f69-b25d4813f28d">IFaxDocument::get_ScheduleType</a>



<a href="https://msdn.microsoft.com/5bb282da-3226-4c9d-ab75-82a587b0a56f">IFaxOutgoingQueue::get_DiscountRateEnd</a>



<a href="https://msdn.microsoft.com/8df89f09-8fba-4bad-a516-82ab471d189e">IFaxOutgoingQueue::get_DiscountRateStart</a>
 

 

