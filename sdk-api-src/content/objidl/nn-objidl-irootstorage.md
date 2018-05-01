---
UID: NN:objidl.IRootStorage
title: IRootStorage
author: windows-driver-content
description: The IRootStorage interface contains a single method that switches a storage object to a different underlying file and saves the storage object to that file.
old-location: stg\irootstorage.htm
old-project: Stg
ms.assetid: cf92c62f-ef65-46b1-8f41-f2b31ff52044
ms.author: windowsdriverdev
ms.date: 4/20/2018
ms.keywords: IRootStorage, IRootStorage interface [Structured Storage], IRootStorage interface [Structured Storage], described, _stg_irootstorage, objidl/IRootStorage, stg.irootstorage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: THDTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Ole32.dll
api_name:
-	IRootStorage
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IRootStorage interface


## -description



			The 
<b>IRootStorage</b> interface contains a single method that switches a storage object to a different underlying file and saves the storage object to that file. The save operation occurs even with low-memory conditions and uncommitted changes to the storage object. A subsequent call to 
<a href="https://msdn.microsoft.com/72831f2c-1e07-429b-af4c-2aaced3f3888">IStorage::Commit</a> is guaranteed to not consume additional memory.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRootStorage</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IRootStorage</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRootStorage</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d482b51a-7159-4aab-ac5e-3f1878d426b2">SwitchToFile</a>
</td>
<td align="left" width="63%">
Copies the file underlying this root storage object, and then associates this storage with the copied file.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a>



<a href="https://msdn.microsoft.com/3292484b-8eff-438d-b989-b58ae323872b">StgCreateDocfile</a>
 

 

