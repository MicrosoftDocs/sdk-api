---
UID: NF:cmnquery.IPersistQuery.WriteString
title: IPersistQuery::WriteString
author: windows-sdk-content
description: Writes a string to the query store.
old-location: ad\ipersistquery_writestring.htm
old-project: ad
ms.assetid: 6bf8499a-6b3a-4786-8d42-67ab4e1a40c0
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IPersistQuery interface [Active Directory],WriteString method, IPersistQuery.WriteString, IPersistQuery::WriteString, WriteString, WriteString method [Active Directory], WriteString method [Active Directory],IPersistQuery interface, _glines_ipersistquery_writestring, ad.ipersistquery__writestring, ad.ipersistquery_writestring, cmnquery/IPersistQuery::WriteString
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: cmnquery.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: DBTEXT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dsquery.dll
api_name:
 - IPersistQuery.WriteString
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Dsquery.dll
req.irql: 
---

# IPersistQuery::WriteString


## -description


The <b>IPersistQuery::WriteString</b> method writes a string to the query store.


## -parameters




### -param pSection [in]

Pointer to a null-terminated Unicode string that represents the section name that the string should be written to.


### -param pValueName [in]

Pointer to a null-terminated Unicode string that represents the name of the string value.


### -param pValue [in]

Pointer to a null-terminated Unicode string that contains the string to be written.


## -returns



Returns <b>S_OK</b> if successful or a standard  <b>HRESULT</b> value otherwise. Possible error codes include the following.




## -see-also




<a href="https://msdn.microsoft.com/f53d4425-5496-45f8-a09b-f163b63a29c8">Display Interfaces in Active Directory Domain Services</a>



<a href="https://msdn.microsoft.com/9d90f119-3d10-4f06-bed4-5ffab9ae14a4">IPersistQuery</a>
 

 

