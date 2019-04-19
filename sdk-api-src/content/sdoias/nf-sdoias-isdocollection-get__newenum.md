---
UID: NF:sdoias.ISdoCollection.get__NewEnum
title: ISdoCollection::get__NewEnum (sdoias.h)
author: windows-sdk-content
description: The get__NewEnum method retrieves an IEnumVARIANT interface for a Server Data Objects (SDO) collection.
old-location: nps\SDO_isdocollection_get__newenum.htm
tech.root: Nps
ms.assetid: f41211cf-7ed6-4f49-ba90-a72b6eb4db3e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISdoCollection interface [Network Policy Server],get__NewEnum method, ISdoCollection.get__NewEnum, ISdoCollection::get__NewEnum, _sdo_isdocollection_get__newenum, get__NewEnum, get__NewEnum method [Network Policy Server], get__NewEnum method [Network Policy Server],ISdoCollection interface, nps.SDO_isdocollection_get__newenum, sdo.isdocollection_get__newenum, sdoias/ISdoCollection::get__NewEnum
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
 - ISdoCollection.get__NewEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISdoCollection::get__NewEnum


## -description


The 
<b>get__NewEnum</b> method retrieves an 
<a href="https://msdn.microsoft.com/en-us/library/ms221053(v=VS.85).aspx">IEnumVARIANT</a> interface for a Server Data Objects (SDO) collection.


## -parameters




### -param ppEnumVARIANT [out]

Pointer to an 
<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface pointer. On successful return the <b>IUnknown</b> interface pointer, points to an 
<a href="https://msdn.microsoft.com/en-us/library/ms221053(v=VS.85).aspx">IEnumVARIANT</a> interface.

This parameter must not be <b>NULL</b>.


## -returns



If the method succeeds the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.




## -remarks



Initialize the SDO before calling this method.

<div class="alert"><b>Note</b>  Two underscores are used between "get" and "NewEnum" in the name of this method.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/26470906-1cba-41fc-96f3-078208ab3d51">ISdoCollection</a>
 

 

