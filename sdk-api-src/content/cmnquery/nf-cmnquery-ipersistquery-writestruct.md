---
UID: NF:cmnquery.IPersistQuery.WriteStruct
title: IPersistQuery::WriteStruct
author: windows-sdk-content
description: Writes a structure to the query store.
old-location: ad\ipersistquery_writestruct.htm
tech.root: ad
ms.assetid: c0acd6c7-96ee-4650-9cfc-3bad4fdffdcc
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IPersistQuery interface [Active Directory],WriteStruct method, IPersistQuery.WriteStruct, IPersistQuery::WriteStruct, WriteStruct, WriteStruct method [Active Directory], WriteStruct method [Active Directory],IPersistQuery interface, _glines_ipersistquery_writestruct, ad.ipersistquery__writestruct, ad.ipersistquery_writestruct, cmnquery/IPersistQuery::WriteStruct
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
 - IPersistQuery.WriteStruct
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPersistQuery::WriteStruct


## -description


The <b>IPersistQuery::WriteStruct</b> method writes a structure to the query store.


## -parameters




### -param pSection [in]

Pointer to a null-terminated Unicode string that represents the section name that the structure should be written to.


### -param pValueName [in]

Pointer to a null-terminated Unicode string that represents the name of the structure.


### -param pStruct [in]

Pointer to the structure to be written. The <i>cbStruct</i> parameter contains the number of bytes to be written.


### -param cbStruct [in]

Contains the size, in bytes, of the structure to be written.


## -returns



Returns <b>S_OK</b> if successful or a standard  <b>HRESULT</b> value otherwise. Possible error codes include the following.




## -see-also




<a href="https://msdn.microsoft.com/f53d4425-5496-45f8-a09b-f163b63a29c8">Display Interfaces in Active Directory Domain Services</a>



<a href="https://msdn.microsoft.com/9d90f119-3d10-4f06-bed4-5ffab9ae14a4">IPersistQuery</a>
 

 

