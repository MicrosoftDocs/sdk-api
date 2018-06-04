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

# QOS_OBJECT_HDR structure


## -description


The QOS object 
<b>QOS_OBJECT_HDR</b> is attached to each QOS object. It specifies the object type and its length.


## -struct-fields




### -field ObjectType

Specifies the type of object to which 
<b>QOS_OBJECT_HDR</b> is attached. The following values are valid for 
<b>QOS_OBJECT_HDR</b>: 




<a id="QOS_OBJECT_DESTADDR"></a>
<a id="qos_object_destaddr"></a>


#### QOS_OBJECT_DESTADDR

<a id="QOS_OBJECT_END_OF_LIST"></a>
<a id="qos_object_end_of_list"></a>


#### QOS_OBJECT_END_OF_LIST

<a id="QOS_OBJECT_SD_MODE"></a>
<a id="qos_object_sd_mode"></a>


#### QOS_OBJECT_SD_MODE

<a id="QOS_OBJECT_SHAPING_RATE"></a>
<a id="qos_object_shaping_rate"></a>


#### QOS_OBJECT_SHAPING_RATE

<a id="RSVP_OBJECT_ADSPEC"></a>
<a id="rsvp_object_adspec"></a>


#### RSVP_OBJECT_ADSPEC

<a id="RSVP_OBJECT_FILTERSPEC_LIST"></a>
<a id="rsvp_object_filterspec_list"></a>


#### RSVP_OBJECT_FILTERSPEC_LIST

<a id="RSVP_OBJECT_POLICY_INFO"></a>
<a id="rsvp_object_policy_info"></a>


#### RSVP_OBJECT_POLICY_INFO

<a id="RSVP_OBJECT_RESERVE_INFO"></a>
<a id="rsvp_object_reserve_info"></a>


#### RSVP_OBJECT_RESERVE_INFO


### -field ObjectLength

Specifies the length of the attached object, inclusive of QOS_OBJECT_HDR.
					


## -see-also




<a href="https://msdn.microsoft.com/859faa13-bd66-46ee-8452-6ff5d53d66c9">QOS</a>
 

 

