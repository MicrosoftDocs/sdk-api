---
UID: NF:cmnquery.IPersistQuery.WriteInt
title: IPersistQuery::WriteInt
author: windows-sdk-content
description: Writes an integer value to the query store.
old-location: ad\ipersistquery_writeint.htm
tech.root: ad
ms.assetid: 5f68865a-dd9f-4428-9cbc-f998f0f1f4a7
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: IPersistQuery interface [Active Directory],WriteInt method, IPersistQuery.WriteInt, IPersistQuery::WriteInt, WriteInt, WriteInt method [Active Directory], WriteInt method [Active Directory],IPersistQuery interface, _glines_ipersistquery_writeint, ad.ipersistquery__writeint, ad.ipersistquery_writeint, cmnquery/IPersistQuery::WriteInt
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
 - IPersistQuery.WriteInt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPersistQuery::WriteInt


## -description


The <b>IPersistQuery::WriteInt</b> method writes an integer value to the query store.


## -parameters




### -param pSection [in]

Pointer to a null-terminated Unicode string that represents the section name that the integer should be written to.


### -param pValueName [in]

Pointer to a null-terminated Unicode string that represents the name of the integer value.


### -param value [in]

Contains the integer value to be written to the query store.


## -returns



Returns <b>S_OK</b> if successful or a standard  <b>HRESULT</b> value otherwise. Possible error codes include the following.




## -see-also




<a href="https://msdn.microsoft.com/f53d4425-5496-45f8-a09b-f163b63a29c8">Display Interfaces in Active Directory Domain Services</a>



<a href="https://msdn.microsoft.com/9d90f119-3d10-4f06-bed4-5ffab9ae14a4">IPersistQuery</a>
 

 

