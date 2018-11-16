---
UID: NE:comsvcs.tagCSC_ThreadPool
title: tagCSC_ThreadPool
author: windows-sdk-content
description: Indicates the thread pool in which the work runs that is submitted through the activity returned from CoCreateActivity.
old-location: cos\csc_threadpool.htm
tech.root: cossdk
ms.assetid: 5acf5c6b-b015-448b-ad4c-e4361a97c31e
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CSC_MTAThreadPool, CSC_STAThreadPool, CSC_ThreadPool, CSC_ThreadPool enumeration [COM+], CSC_ThreadPoolInherit, CSC_ThreadPoolNone, _cos_CSC_ThreadPool, comsvcs/CSC_MTAThreadPool, comsvcs/CSC_STAThreadPool, comsvcs/CSC_ThreadPool, comsvcs/CSC_ThreadPoolInherit, comsvcs/CSC_ThreadPoolNone, cos.csc_threadpool, tagCSC_ThreadPool
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ComSvcs.h
api_name:
 - CSC_ThreadPool
product: Windows
targetos: Windows
req.typenames: CSC_ThreadPool
req.redist: 
---

# tagCSC_ThreadPool enumeration


## -description


Indicates the thread pool in which the work runs that is submitted through the activity returned from <a href="https://msdn.microsoft.com/3009eb4f-e3f3-497b-ba05-5b750d8a40d0">CoCreateActivity</a>.


## -enum-fields




### -field CSC_ThreadPoolNone

No thread pool is used. If this value is used to configure a <a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a> object that is passed to <a href="https://msdn.microsoft.com/3009eb4f-e3f3-497b-ba05-5b750d8a40d0">CoCreateActivity</a>, an error (CO_E_THREADPOOL_CONFIG) is returned. This is the default thread pool setting for <b>CServiceConfig</b> when <a href="https://msdn.microsoft.com/9bc8c4f3-d13e-46b6-9187-904b05f66f66">CSC_InheritanceConfig</a> is set to CSC_Ignore.


### -field CSC_ThreadPoolInherit

The same type of thread pool apartment as the caller's thread apartment is used. If the caller's thread apartment is the neutral apartment, a single-threaded apartment is used. This is the default thread pool setting for <a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a> when <a href="https://msdn.microsoft.com/9bc8c4f3-d13e-46b6-9187-904b05f66f66">CSC_InheritanceConfig</a> is set to CSC_Inherit.


### -field CSC_STAThreadPool

A single-threaded apartment (STA) is used.


### -field CSC_MTAThreadPool

A multithreaded apartment (MTA) is used.


## -remarks



This enumeration is used to set the thread pool for <a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a> only when calling <a href="https://msdn.microsoft.com/3009eb4f-e3f3-497b-ba05-5b750d8a40d0">CoCreateActivity</a>. An error is returned if you try to set the thread pool when calling <a href="https://msdn.microsoft.com/84640b3b-1f43-4bec-abf6-c295cfb3da8b">CoEnterServiceDomain</a>.




## -see-also




<a href="https://msdn.microsoft.com/c73fb4c5-20ae-4873-afd2-4f40eb47bade">COM+ Threading Models</a>



<a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a>



<a href="https://msdn.microsoft.com/3009eb4f-e3f3-497b-ba05-5b750d8a40d0">CoCreateActivity</a>



<a href="https://msdn.microsoft.com/eba8b4fc-aee7-4ba5-8e0e-b74ce9d25a86">IServiceThreadPoolConfig::SelectThreadPool</a>
 

 

