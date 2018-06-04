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

# _SID_INFO_LIST structure


## -description


The <b>SID_INFO_LIST</b> structure contains a list of 
<a href="https://msdn.microsoft.com/6a69e5b9-ab6a-4bbb-9f1a-5882d4c8038c">SID_INFO</a> structures.


## -struct-fields




### -field cItems

The number of 
<a href="https://msdn.microsoft.com/6a69e5b9-ab6a-4bbb-9f1a-5882d4c8038c">SID_INFO</a> structures contained in the <b>aSidInfo</b> member.


### -field aSidInfo

A pointer to a list of <a href="https://msdn.microsoft.com/6a69e5b9-ab6a-4bbb-9f1a-5882d4c8038c">SID_INFO</a> structures that is returned by the 
<a href="https://msdn.microsoft.com/9a4056c6-6a21-4051-b4a6-c77351fce983">ISecurityInformation2::LookupSids</a> method.


## -see-also




<a href="https://msdn.microsoft.com/9a4056c6-6a21-4051-b4a6-c77351fce983">ISecurityInformation2::LookupSids</a>



<a href="https://msdn.microsoft.com/6a69e5b9-ab6a-4bbb-9f1a-5882d4c8038c">SID_INFO</a>
 

 

