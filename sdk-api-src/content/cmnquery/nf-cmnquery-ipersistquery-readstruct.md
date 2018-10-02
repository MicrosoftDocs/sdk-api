---
UID: NF:cmnquery.IPersistQuery.ReadStruct
title: IPersistQuery::ReadStruct
author: windows-sdk-content
description: Reads a structure from the query store.
old-location: ad\ipersistquery_readstruct.htm
tech.root: AD
ms.assetid: 47d1b733-7e37-42f8-b344-909a6e48b381
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IPersistQuery interface [Active Directory],ReadStruct method, IPersistQuery.ReadStruct, IPersistQuery::ReadStruct, ReadStruct, ReadStruct method [Active Directory], ReadStruct method [Active Directory],IPersistQuery interface, _glines_ipersistquery_readstruct, ad.ipersistquery__readstruct, ad.ipersistquery_readstruct, cmnquery/IPersistQuery::ReadStruct
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: cmnquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Dsquery.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dsquery.dll
api_name:
 - IPersistQuery.ReadStruct
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPersistQuery::ReadStruct


## -description


The <b>IPersistQuery::ReadStruct</b> method reads a structure from the query store.


## -parameters




### -param pSection [in]

Pointer to a null-terminated Unicode string that represents the section name that the structure should be read from.


### -param pValueName [in]

Pointer to a null-terminated Unicode string that represents the name of the structure value to be read.


### -param pStruct [out]

Pointer to a buffer that will receive the structure. The <i>cbStruct</i> parameter specifies the size of this buffer, in bytes.


### -param cbStruct [in]

Specifies the size, in bytes, of the  buffer represented by the <i>pStruct</i> parameter.


## -returns



Returns <b>S_OK</b> if successful or a standard  <b>HRESULT</b> value otherwise. Possible error codes include the following.




## -see-also




<a href="https://msdn.microsoft.com/f53d4425-5496-45f8-a09b-f163b63a29c8">Display Interfaces in Active Directory Domain Services</a>



<a href="https://msdn.microsoft.com/9d90f119-3d10-4f06-bed4-5ffab9ae14a4">IPersistQuery</a>
 

 

