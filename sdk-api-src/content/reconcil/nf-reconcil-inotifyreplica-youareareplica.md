---
UID: NF:reconcil.INotifyReplica.YouAreAReplica
title: INotifyReplica::YouAreAReplica (reconcil.h)
author: windows-sdk-content
description: Notifies an object that it may be subject to subsequent reconciliation through the Reconcile method.
old-location: shell\INotifyReplica_YouAreAReplica.htm
tech.root: shell
ms.assetid: e6cbdb94-1804-4d6d-890e-d3fd596fec89
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: INotifyReplica interface [Windows Shell],YouAreAReplica method, INotifyReplica.YouAreAReplica, INotifyReplica::YouAreAReplica, YouAreAReplica, YouAreAReplica method [Windows Shell], YouAreAReplica method [Windows Shell],INotifyReplica interface, _win32_INotifyReplica_YouAreAReplica, reconcil/INotifyReplica::YouAreAReplica, shell.INotifyReplica_YouAreAReplica
ms.topic: method
req.header: reconcil.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - INotifyReplica.YouAreAReplica
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INotifyReplica::YouAreAReplica


## -description


Notifies an object that it may be subject to subsequent reconciliation through the <a href="https://msdn.microsoft.com/6dfeb68e-fd23-4812-8a3c-ab27fc00a4ad">Reconcile</a> method.


## -parameters




### -param ulcOtherReplicas

Type: <b>ULONG</b>

The number of other replicas of the object. This parameter must not be zero.


### -param rgpmkOtherReplicas

Type: <b><a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a>**</b>

The address of an array that contains the addresses of the monikers to use to access the other replicas.


## -returns



Type: <b>HRESULT</b>

Returns <b>S_OK</b> if successful, or <b>E_UNEXPECTED</b> otherwise.




## -remarks



An object may be notified that it is a replica more than once. Briefcase reconcilers are not required to implement this interface. Initiators are not required to call this interface if it is implemented. However, an object's implementation of <a href="https://msdn.microsoft.com/6dfeb68e-fd23-4812-8a3c-ab27fc00a4ad">Reconcile</a> may fail if that object has not previously been notified through <b>INotifyReplica::YouAreAReplica</b> that it may be subject to reconciliation.

The briefcase calls the <a href="https://msdn.microsoft.com/aa04d5b0-8483-4024-91d0-65d69d6891ca">INotifyReplica</a> interface when objects are added to it.



