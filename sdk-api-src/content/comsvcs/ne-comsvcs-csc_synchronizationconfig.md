---
UID: NE:comsvcs.tagCSC_SynchronizationConfig
title: CSC_SynchronizationConfig (comsvcs.h)
author: windows-sdk-content
description: Indicates how synchronization is configured for CServiceConfig.
old-location: cos\csc_synchronizationconfig.htm
tech.root: cossdk
ms.assetid: dc0c4310-e2d8-462c-af55-f1513934b8ef
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CSC_IfContainerIsSynchronized, CSC_NewSynchronization, CSC_NewSynchronizationIfNecessary, CSC_NoSynchronization, CSC_SynchronizationConfig, CSC_SynchronizationConfig enumeration [COM+], _cos_CSC_SynchronizationConfig, comsvcs/CSC_IfContainerIsSynchronized, comsvcs/CSC_NewSynchronization, comsvcs/CSC_NewSynchronizationIfNecessary, comsvcs/CSC_NoSynchronization, comsvcs/CSC_SynchronizationConfig, cos.csc_synchronizationconfig
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
 - CSC_SynchronizationConfig
product: Windows
targetos: Windows
req.typenames: CSC_SynchronizationConfig
req.redist: 
---

# CSC_SynchronizationConfig enumeration


## -description


Indicates how synchronization is configured for <a href="https://msdn.microsoft.com/en-us/library/ms688295(v=VS.85).aspx">CServiceConfig</a>.


## -enum-fields




### -field CSC_NoSynchronization

The code is forced to run unsynchronized. This is the default synchronization setting for <a href="https://msdn.microsoft.com/en-us/library/ms688295(v=VS.85).aspx">CServiceConfig</a> when <a href="https://msdn.microsoft.com/9bc8c4f3-d13e-46b6-9187-904b05f66f66">CSC_InheritanceConfig</a> is set to CSC_Ignore.


### -field CSC_IfContainerIsSynchronized

The code runs in the containing synchronization domain if one exists. This is the default synchronization setting for <a href="https://msdn.microsoft.com/en-us/library/ms688295(v=VS.85).aspx">CServiceConfig</a> when <a href="https://msdn.microsoft.com/9bc8c4f3-d13e-46b6-9187-904b05f66f66">CSC_InheritanceConfig</a> is set to CSC_Inherit.


### -field CSC_NewSynchronizationIfNecessary

Synchronization is always used. The existing synchronization domain is used, or if the enclosed context does not already use synchronization, a new synchronization domain is created.


### -field CSC_NewSynchronization

A new synchronization domain is always created.


## -remarks



This enumeration is used to configure synchronization through <a href="https://msdn.microsoft.com/en-us/library/ms688295(v=VS.85).aspx">CServiceConfig</a> for either the work submitted through the activity created by <a href="https://msdn.microsoft.com/3009eb4f-e3f3-497b-ba05-5b750d8a40d0">CoCreateActivity</a> or the work that is enclosed between calls to <a href="https://msdn.microsoft.com/84640b3b-1f43-4bec-abf6-c295cfb3da8b">CoEnterServiceDomain</a> and <a href="https://msdn.microsoft.com/b67b3cf6-4462-4578-b61b-c5c61d809822">CoLeaveServiceDomain</a>.

Synchronization can affect the components created by the contained code even if it has no immediate impact on the contained code itself. For example, if the same code is running on two different threads and this code calls <a href="https://msdn.microsoft.com/84640b3b-1f43-4bec-abf6-c295cfb3da8b">CoEnterServiceDomain</a> asking for synchronization services, each thread is contained in its own synchronization domain.

If it is incompatible with the transaction setting from <a href="https://msdn.microsoft.com/3524d7b3-4bcd-4e92-afc2-ddac98a23b7c">CSC_TransactionConfig</a>, the synchronization setting is increased to the minimum that is required for the transaction.




## -see-also




<a href="https://msdn.microsoft.com/a348959a-fa23-495c-ba1c-85bc3ae92396">COM+ Synchronization</a>



<a href="https://msdn.microsoft.com/en-us/library/ms688295(v=VS.85).aspx">CServiceConfig</a>



<a href="https://msdn.microsoft.com/3009eb4f-e3f3-497b-ba05-5b750d8a40d0">CoCreateActivity</a>



<a href="https://msdn.microsoft.com/84640b3b-1f43-4bec-abf6-c295cfb3da8b">CoEnterServiceDomain</a>



<a href="https://msdn.microsoft.com/83fe6958-6639-4468-a3f5-3322316ccbc4">IServiceSynchronizationConfig::ConfigureSynchronization</a>
 

 

