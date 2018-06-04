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

# DashStyle enumeration


## -description


The <b>DashStyle</b> enumeration specifies the line style of a line drawn with a Windows GDI+ pen. The line can be drawn by using one of several predefined styles or a custom style.


## -enum-fields




### -field DashStyleSolid

Specifies a solid line. 


### -field DashStyleDash

Specifies a dashed line. 


### -field DashStyleDot

Specifies a dotted line. 


### -field DashStyleDashDot

Specifies an alternating dash-dot line. 


### -field DashStyleDashDotDot

Specifies an alternating dash-dot-dot line. 


### -field DashStyleCustom

Specifies a user-defined, custom dashed line. 


## -remarks



A custom dashed line is created by calling the 
				<a href="https://msdn.microsoft.com/bfddd867-a2b1-4f2b-9c99-cc2112e13fa0">Pen::SetDashPattern</a> method, which takes an array of values for the dash lengths and the space lengths.



