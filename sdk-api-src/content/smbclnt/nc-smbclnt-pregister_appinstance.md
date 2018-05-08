---
UID: NC:smbclnt.PREGISTER_APPINSTANCE
title: PREGISTER_APPINSTANCE
author: windows-driver-content
description: Registers the AppInstance ID for a process.
old-location: mscs\registerappinstance.htm
old-project: MsCS
ms.assetid: 43CAC59A-5773-44BD-8965-F9FB85B86926
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: PREGISTER_APPINSTANCE, PREGISTER_APPINSTANCE callback, PREGISTER_APPINSTANCE callback function [Failover Cluster], mscs.registerappinstance, smbclnt/PREGISTER_APPINSTANCE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: smbclnt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SL_NONGENUINE_UI_OPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	SmbClnt.h
api_name:
-	PREGISTER_APPINSTANCE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
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
 

 

