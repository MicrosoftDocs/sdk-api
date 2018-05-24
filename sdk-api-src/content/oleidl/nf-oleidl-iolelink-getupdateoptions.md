---
UID: NF:oleidl.IOleLink.GetUpdateOptions
title: IOleLink::GetUpdateOptions
author: windows-driver-content
description: Retrieves a value indicating how often the linked object updates its cached data.
old-location: com\iolelink_getupdateoptions.htm
old-project: com
ms.assetid: 2cb91b48-0026-4afa-80ab-16ac6fbce04d
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: GetUpdateOptions, GetUpdateOptions method [COM], GetUpdateOptions method [COM],IOleLink interface, IOleLink interface [COM],GetUpdateOptions method, IOleLink.GetUpdateOptions, IOleLink::GetUpdateOptions, _ole_iolelink_getupdateoptions, com.iolelink_getupdateoptions, oleidl/IOleLink::GetUpdateOptions
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: USERCLASSTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	OleIdl.h
api_name:
-	IOleLink.GetUpdateOptions
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOleLink::GetUpdateOptions


## -description


Retrieves a value indicating how often the linked object updates its cached data.


## -parameters




### -param pdwUpdateOpt [out]

A pointer to a variable that receives the current value for the linked object's update option, indicating how often the linked object updates the cached data for the linked object. The possible values for <i>pdwUpdateOpt</i> are taken from the enumeration <a href="https://msdn.microsoft.com/1945d4a2-dd1f-453e-ab7e-093f26171c84">OLEUPDATE</a>.


## -returns



This method returns S_OK on success.




## -see-also




<a href="https://msdn.microsoft.com/4a34a90d-df1b-4bbf-8365-9d741c18ff74">IOleLink</a>



<a href="https://msdn.microsoft.com/310c25b5-a2f6-4ed7-8673-c53809fad32f">IOleLink::SetUpdateOptions</a>



<a href="https://msdn.microsoft.com/7fc0aab3-7476-49ec-8a1d-3f4851f9f31c">IOleUILinkContainer</a>



<a href="https://msdn.microsoft.com/17c7daf8-83bf-4cfd-a67c-a638630ca263">OleUIEditLinks</a>
 

 

