---
UID: NF:comsvcs.IComInstance2Events.OnObjectCreate2
title: IComInstance2Events::OnObjectCreate2 (comsvcs.h)
author: windows-sdk-content
description: Generated when a client creates an object.
old-location: cos\icominstance2events_onobjectcreate2.htm
tech.root: cossdk
ms.assetid: b7c359b8-2d49-4982-836b-50d749758fa6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IComInstance2Events interface [COM+],OnObjectCreate2 method, IComInstance2Events.OnObjectCreate2, IComInstance2Events::OnObjectCreate2, OnObjectCreate2, OnObjectCreate2 method [COM+], OnObjectCreate2 method [COM+],IComInstance2Events interface, _dtc_IComInstance2Events_OnObjectCreate2, comsvcs/IComInstance2Events::OnObjectCreate2, cos.icominstance2events_onobjectcreate2
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IComInstance2Events.OnObjectCreate2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComInstance2Events::OnObjectCreate2


## -description


Generated when a client creates an object.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms688276(v=VS.85).aspx">COMSVCSEVENTINFO</a> structure.


### -param guidActivity [in]

The identifier of the activity in which the object is created.


### -param clsid [in]

The CLSID of the object being created.


### -param tsid [in]

The transaction stream identifier, which is unique for correlation to objects.


### -param CtxtID [in]

The context identifier for this object.


### -param ObjectID [in]

The initial JIT-activated object.


### -param guidPartition [in]

The partition identifier for which this instance is created.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms679548(v=VS.85).aspx">IComInstance2Events</a>
 

 

