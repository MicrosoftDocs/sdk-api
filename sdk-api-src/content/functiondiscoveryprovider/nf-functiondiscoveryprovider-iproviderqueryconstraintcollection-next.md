---
UID: NF:functiondiscoveryprovider.IProviderQueryConstraintCollection.Next
title: IProviderQueryConstraintCollection::Next
author: windows-sdk-content
description: Gets the name and value of the next query constraint in the collection.
old-location: ncd\iproviderqueryconstraintcollection_next.htm
tech.root: fundisc
ms.assetid: 5dd03e98-5367-4434-aa68-be36cb7aaf24
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: IProviderQueryConstraintCollection interface,Next method, IProviderQueryConstraintCollection.Next, IProviderQueryConstraintCollection::Next, Next, Next method, Next method,IProviderQueryConstraintCollection interface, functiondiscoveryprovider/IProviderQueryConstraintCollection::Next, ncd.iproviderqueryconstraintcollection_next
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: functiondiscoveryprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FunctionDiscoveryProvider.idl
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
 - COM
api_location:
 - FunctionDiscoveryProvider.h
api_name:
 - IProviderQueryConstraintCollection.Next
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IProviderQueryConstraintCollection::Next


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Gets the name and value of the next query  constraint in the collection.


## -parameters




### -param ppszConstraintName [out]

The constraint name.


### -param ppszConstraintValue [out]

The constraint value.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/4d8ff5b9-ec4a-4ec6-b133-3d315f9c017b">IProviderQueryConstraintCollection</a>
 

 

