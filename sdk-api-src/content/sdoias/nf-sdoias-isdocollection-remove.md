---
UID: NF:sdoias.ISdoCollection.Remove
title: ISdoCollection::Remove
author: windows-sdk-content
description: The Remove method removes the specified item from the collection.
old-location: nps\SDO_isdocollection_remove.htm
tech.root: Nps
ms.assetid: f390377d-b78e-4548-9602-c0eb363765c7
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ISdoCollection interface [Network Policy Server],Remove method, ISdoCollection.Remove, ISdoCollection::Remove, Remove, Remove method [Network Policy Server], Remove method [Network Policy Server],ISdoCollection interface, _sdo_isdocollection_remove, nps.SDO_isdocollection_remove, sdo.isdocollection_remove, sdoias/ISdoCollection::Remove
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: sdoias.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: SdoIas.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Iassdo.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Iassdo.dll
api_name:
 - ISdoCollection.Remove
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- sdoias.h
: 
- ISdoCollection.Remove
: 
---

# ISdoCollection::Remove


## -description


The 
<b>Remove</b> method removes the specified item from the collection.


## -parameters




### -param pItem [in]

Pointer to an 
<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface that specifies the item to remove.

This parameter must not be <b>NULL</b>.


## -returns



If the method succeeds the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.




## -see-also




<a href="https://msdn.microsoft.com/26470906-1cba-41fc-96f3-078208ab3d51">ISdoCollection</a>



<a href="https://msdn.microsoft.com/a575b224-9827-47f3-a819-bd793200c901">ISdoCollection::Add</a>



<a href="https://msdn.microsoft.com/82654df4-9a85-4687-86dd-04ea5a916fdc">ISdoCollection::RemoveAll</a>
 

 

