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

# IFsrmPathMapper::GetSharePathsForLocalPath


## -description


Retrieves a list of network shares that point to the specified local path.


## -parameters




### -param localPath [in]

The local path. The string is limited to 260 characters.


### -param sharePaths [out]

A <b>SAFEARRAY</b> of <b>VARIANT</b>s. Each 
      <b>VARIANT</b> contains a network share path that points to the local path. The variant 
      type is <b>VT_BSTR</b>. Use the <b>bstrVal</b> member to access the share 
      path.


## -returns



The method returns the following return values.




## -remarks



When you get the path property for a quota, the path is the local path. You use this method to convert that 
    local path to the network path if you want to know the actual network share that is running out of space.




## -see-also




<a href="https://msdn.microsoft.com/19f7f1d1-7d10-4b73-a158-7c8722958ab5">FsrmPathMapper</a>



<a href="https://msdn.microsoft.com/04e62a10-1719-454b-adfb-6320e31c7a88">IFsrmPathMapper</a>
 

 

