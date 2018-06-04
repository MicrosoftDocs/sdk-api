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

# _VSS_MGMT_OBJECT_TYPE enumeration


## -description


The <b>VSS_MGMT_OBJECT_TYPE</b> enumeration type is a 
    discriminant for the <a href="https://msdn.microsoft.com/4d787229-671a-422c-a935-39ae11073a5e">VSS_MGMT_OBJECT_UNION</a> 
    union within the <a href="https://msdn.microsoft.com/86681207-969e-4b33-aff8-79454ab04829">VSS_MGMT_OBJECT_PROP</a> 
    structure.


## -enum-fields




### -field VSS_MGMT_OBJECT_UNKNOWN

The object type is unknown.


### -field VSS_MGMT_OBJECT_VOLUME

The object is a volume to be shadow copied.


### -field VSS_MGMT_OBJECT_DIFF_VOLUME

The object is a volume to hold a shadow copy storage area.


### -field VSS_MGMT_OBJECT_DIFF_AREA

The object is an association between a volume to be shadow copied and a volume to hold the shadow copy 
      storage area.


## -see-also




<a href="https://msdn.microsoft.com/86681207-969e-4b33-aff8-79454ab04829">VSS_MGMT_OBJECT_PROP</a>



<a href="https://msdn.microsoft.com/4d787229-671a-422c-a935-39ae11073a5e">VSS_MGMT_OBJECT_UNION</a>
 

 

