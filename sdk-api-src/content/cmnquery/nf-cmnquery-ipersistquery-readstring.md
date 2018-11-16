---
UID: NF:cmnquery.IPersistQuery.ReadString
title: IPersistQuery::ReadString
author: windows-sdk-content
description: Reads a string from the query store.
old-location: ad\ipersistquery_readstring.htm
tech.root: ad
ms.assetid: 5d96234f-080e-49c6-ae31-c4eb672ecf04
ms.author: windowssdkdev
ms.date: 11/14/2018
ms.keywords: IPersistQuery interface [Active Directory],ReadString method, IPersistQuery.ReadString, IPersistQuery::ReadString, ReadString, ReadString method [Active Directory], ReadString method [Active Directory],IPersistQuery interface, _glines_ipersistquery_readstring, ad.ipersistquery__readstring, ad.ipersistquery_readstring, cmnquery/IPersistQuery::ReadString
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
 - IPersistQuery.ReadString
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- cmnquery.h
: 
- IPersistQuery.ReadString
: 
---

# IPersistQuery::ReadString


## -description


The <b>IPersistQuery::ReadString</b> method reads a string from the query store.


## -parameters




### -param pSection [in]

Pointer to a null-terminated Unicode string that represents the section name that the string should be read from.


### -param pValueName [in]

Pointer to a null-terminated Unicode string that represents the name of the string value to be read.


### -param pBuffer [out]

Pointer to a character buffer that receives the string value. The <i>cchBuffer</i> parameter specifies the size of this buffer including the null terminator.


### -param cchBuffer [in]

Contains the size, in characters, of the <i>pBuffer</i> buffer including the null terminator.


## -returns



Returns <b>S_OK</b> if successful or a standard  <b>HRESULT</b> value otherwise. Possible error codes include the following.




## -see-also




<a href="https://msdn.microsoft.com/f53d4425-5496-45f8-a09b-f163b63a29c8">Display Interfaces in Active Directory Domain Services</a>



<a href="https://msdn.microsoft.com/9d90f119-3d10-4f06-bed4-5ffab9ae14a4">IPersistQuery</a>
 

 

