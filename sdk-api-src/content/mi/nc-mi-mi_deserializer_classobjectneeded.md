---
UID: NC:mi.MI_Deserializer_ClassObjectNeeded
title: MI_Deserializer_ClassObjectNeeded (mi.h)
author: windows-sdk-content
description: Used to provide requested class object during deserialization.
old-location: wmi_v2\mi_deserializer_classobjectneeded.htm
tech.root: wmi_v2
ms.assetid: 0C813AAF-99B4-4DA7-9C2F-CD9FA146D7D2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MI_Deserializer_ClassObjectNeeded, MI_Deserializer_ClassObjectNeeded callback, MI_Deserializer_ClassObjectNeeded callback function [Windows Management Infrastructure (MI)], mi/MI_Deserializer_ClassObjectNeeded, wmi_v2.mi_deserializer_classobjectneeded
ms.topic: callback
f1_keywords: 
 - "mi/MI_Deserializer_ClassObjectNeeded"
req.header: mi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - UserDefined
api_location:
 - Mi.h
api_name:
 - MI_Deserializer_ClassObjectNeeded
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1,     Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
---

# MI_Deserializer_ClassObjectNeeded callback function


## -description


Used to provide requested class object during deserialization.


## -parameters




### -param *context [in, optional]

A pointer to the context.


### -param *serverName [in, optional]

The name of the server.


### -param *namespaceName [in, optional]

The namespace of the object.


### -param *className [in, optional]

The class of the object.


#### - **requestedClassObject [out]

A <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/ns-mi-_mi_class">MI_Class</a> representing the requested class object.


#### - requestedClassObject [out]

A <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/ns-mi-_mi_class">MI_Class</a> representing the requested class object.


## -returns



Returns a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/ne-mi-_mi_result">MI_Result</a> indicating the status of the operation.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/ns-mi-_mi_deserializerft">MI_DeserializerFT</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_deserializer_deserializeclass">MI_Deserializer_DeserializeClass</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_deserializer_deserializeinstance">MI_Deserializer_DeserializeInstance</a>
 

 

