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

# _ACL_SIZE_INFORMATION structure


## -description


The <b>ACL_SIZE_INFORMATION</b> structure contains information about the size of an <a href="https://msdn.microsoft.com/library/windows/hardware/ff538866">ACL</a> structure.


## -struct-fields




### -field AceCount

The number of <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control entries</a> (ACEs) in the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control list</a> (ACL).


### -field AclBytesInUse

The number of bytes in the ACL actually used to store the ACEs and <a href="https://msdn.microsoft.com/library/windows/hardware/ff538866">ACL</a> structure. This may be less than the total number of bytes allocated to the ACL.


### -field AclBytesFree

The number of unused bytes in the ACL.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538866">ACL</a>



<a href="https://msdn.microsoft.com/e1abf877-9757-4ee4-b7da-f3e7eb53bddd">ACL_INFORMATION_CLASS</a>



<a href="https://msdn.microsoft.com/cdc7f6b1-aaa1-4893-a192-5a42233b3ec1">ACL_REVISION_INFORMATION</a>



<a href="https://msdn.microsoft.com/23ef6abd-03e9-439e-ba05-629c8d61cd66">GetAclInformation</a>



<a href="https://msdn.microsoft.com/bb4dd7f9-2f15-4a27-89c9-1675f4fb8d92">SetAclInformation</a>
 

 

