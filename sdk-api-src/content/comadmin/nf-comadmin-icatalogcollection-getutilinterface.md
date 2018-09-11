---
UID: NF:comadmin.ICatalogCollection.GetUtilInterface
title: ICatalogCollection::GetUtilInterface
author: windows-sdk-content
description: Retrieves the utility interface for the collection.
old-location: cos\icatalogcollection_getutilinterface.htm
tech.root: cossdk
ms.assetid: bac2153d-253b-4be1-be14-2c1207799ada
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetUtilInterface, GetUtilInterface method [COM+], GetUtilInterface method [COM+],ICatalogCollection interface, ICatalogCollection interface [COM+],GetUtilInterface method, ICatalogCollection.GetUtilInterface, ICatalogCollection::GetUtilInterface, _cos_ICatalogCollection_GetUtilInterface, comadmin/ICatalogCollection::GetUtilInterface, cos.icatalogcollection_getutilinterface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: comadmin.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ComAdmin.Idl
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
 - ComAdmin.h
api_name:
 - ICatalogCollection.GetUtilInterface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICatalogCollection::GetUtilInterface


## -description


<p class="CCE_Message">[This method is for use with MTS 2.0 administration interfaces and objects and should not be used with COM+ administration interfaces and objects. It works as before with MTS 2.0 administration interfaces and objects, with the exception of IRemoteComponentUtil, which is no longer supported.]

Retrieves the utility interface for the collection.


## -parameters




### -param ppIDispatch [out, retval]

The utility interface.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, and E_FAIL, as well as the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>COMADMIN_E_OBJECTERRORS </b></dt>
</dl>
</td>
<td width="60%">
Errors occurred while accessing one or more objects.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms683140(v=VS.85).aspx">ICatalogCollection</a>
 

 

