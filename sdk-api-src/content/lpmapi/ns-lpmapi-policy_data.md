---
UID: NS:lpmapi.POLICY_DATA
title: POLICY_DATA
author: windows-sdk-content
description: The POLICY_DATA structure contains policy data for RSVP messages.
old-location: qos\policy_data.htm
old-project: QOS
ms.assetid: 0e91b77c-e4dd-4e23-8af6-bf549168cfc5
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: POLICY_DATA, POLICY_DATA structure [QOS], lpmapi/POLICY_DATA, qos.policy_data
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: lpmapi.h
req.include-header: 
req.redist: 
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
req.typenames: POLICY_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lpmapi.h
api_name:
 - POLICY_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# POLICY_DATA structure


## -description


The 
<b>POLICY_DATA</b> structure contains policy data for RSVP messages.


## -struct-fields




### -field PolicyObjHdr

Policy object header, in the form of an <a href="https://msdn.microsoft.com/90a237c0-0e62-4f27-927a-e3f3c1ac629e">RsvpObjHdr</a> structure.


### -field usPeOffset

Offset to the beginning of Policy Elements from the beginning of Policy Data.


### -field usReserved

Reserved. Do not use.


## -see-also




<a href="https://msdn.microsoft.com/90a237c0-0e62-4f27-927a-e3f3c1ac629e">RsvpObjHdr</a>
 

 

