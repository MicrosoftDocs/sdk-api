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

# PREGISTER_APPINSTANCE callback function


## -description


Registers the <i>AppInstance</i> ID for a process.


## -parameters




### -param ProcessHandle [in]

A process handle for the current process or a remote process to be tagged with the 
      <i>AppInstanceId</i>. To tag a remote process, the handle must have 
      <b>PROCESS_TERMINATE</b> access to that process.


### -param *AppInstanceId


### -param ChildrenInheritAppInstance [in]

<b>TRUE</b> to tag the child processes spawned by the process specified by 
       <i>ProcessHandle</i>; otherwise, <b>FALSE</b>.


#### - AppInstanceID [in]

The application instance ID, which is a <b>GUID</b>.


## -returns





Returns DWORD that ...






## -remarks



The <i>RegisterAppInstance</i> function issues an 
     <b>IOCTL_CCF_REGISTER_APPINSTANCE</b> call to the CCF mini-filter. The function 
     passes the <i>AppInstance</i> <b>GUID</b>, the 
     process handle, and the tagged child processes to the CCF cache that maps the process handle to the 
     <i>AppInstanceId</i>.

The issued IOCTL for tagging another process checks if the current process has 
     <b>PROCESS_TERMINATE</b> access to the target process.




## -see-also




<a href="https://msdn.microsoft.com/d1f7360d-f592-49fb-b3b4-60d93afd7c6f">Failover Cluster Resource Management Functions</a>
 

 

