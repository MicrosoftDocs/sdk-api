---
UID: NS:qosobjs._QOS_FRIENDLY_NAME
title: "_QOS_FRIENDLY_NAME"
author: windows-sdk-content
description: The QOS_FRIENDLY_NAME traffic control object associates a friendly name with flow.
old-location: qos\qos_friendly_name.htm
old-project: QOS
ms.assetid: 9681fc36-0a31-4b2a-9719-085506126877
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: "*LPQOS_FRIENDLY_NAME, LPQOS_FRIENDLY_NAME, LPQOS_FRIENDLY_NAME structure pointer [QOS], QOS_FRIENDLY_NAME, QOS_FRIENDLY_NAME structure [QOS], _QOS_FRIENDLY_NAME, _gqos_qos_friendly_name, qos.qos_friendly_name, qosobjs/LPQOS_FRIENDLY_NAME, qosobjs/QOS_FRIENDLY_NAME"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: qosobjs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: QOS_FRIENDLY_NAME, *LPQOS_FRIENDLY_NAME
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - QosObjs.h
api_name:
 - QOS_FRIENDLY_NAME
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _QOS_FRIENDLY_NAME structure


## -description


The 
<b>QOS_FRIENDLY_NAME</b> traffic control object associates a friendly name with flow.


## -struct-fields




### -field ObjectHdr

The QOS object 
<a href="https://msdn.microsoft.com/a2021d70-e7ef-4c2a-8800-1a1d7540ce02">QOS_OBJECT_HDR</a>. The object type for this traffic control object should be 
<b>QOS_OBJECT_FRIENDLY_NAME</b>.


### -field FriendlyName

Name to be associated with the flow.


## -remarks



Programmers are encouraged to use the 
<b>QOS_FRIENDLY_NAME</b> traffic control object to associate flows with their applications. This approach enables management applications to identify and associate enumerated flows with corresponding applications.




## -see-also




<a href="https://msdn.microsoft.com/732cfbec-4175-4397-854f-0d2a930e11bc">QOS_DIFFSERV_RULE</a>



<a href="https://msdn.microsoft.com/56eca8ef-2b6e-4380-869c-bf1a4c8fdb1f">QOS_DS_CLASS</a>



<a href="https://msdn.microsoft.com/a2021d70-e7ef-4c2a-8800-1a1d7540ce02">QOS_OBJECT_HDR</a>



<a href="https://msdn.microsoft.com/60c6492f-ddcf-401c-8121-2349b89eb223">QOS_TRAFFIC_CLASS</a>
 

 

