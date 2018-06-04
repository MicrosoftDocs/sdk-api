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

# CLUSTERVERSIONINFO_NT4 structure


## -description


TBD


## -struct-fields




### -field dwVersionInfoSize

Contains the  size, in bytes, of the data structure. Users must set this size prior to calling the  
      <a href="https://msdn.microsoft.com/5b259eb9-c5d0-4f4f-8a6b-14eaed716612">GetClusterInformation</a>   function.


### -field MajorVersion

Identifies the major version number of the operating system that is  installed on the local node. For example, for 
      version X.Y, the major version number is X.


### -field MinorVersion

Identifies the minor version number of the operating system that is  installed on the local node. For example, for 
      version X.Y, the minor version number is Y.


### -field BuildNumber

Identifies the build number of the operating system that is  installed on the local node, such as 224.


### -field szVendorId

Contains the vendor identifier information for the cluster service that is  installed on the local node.


### -field szCSDVersion

Contains the latest service pack that is  installed on the node. If a Service Pack is not installed, the 
      <b>szCSDVersion</b> member is empty.


## -see-also




<a href="https://msdn.microsoft.com/45da8dbc-dd70-4f95-b933-66d8e4340448">Utility Structures</a>
 

 

