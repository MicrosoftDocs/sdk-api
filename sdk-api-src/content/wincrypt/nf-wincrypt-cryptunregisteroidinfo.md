---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# CryptUnregisterOIDInfo function


## -description


The <b>CryptUnregisterOIDInfo</b> function removes the registration of a specified 
<a href="https://msdn.microsoft.com/06ba0f60-778d-450b-8f71-23471b8c4e2c">CRYPT_OID_INFO</a> OID information structure. The structure to be unregistered is identified by the structure's <b>pszOID</b> and <b>dwGroupId</b> members.


## -parameters




### -param pInfo [in]

Specifies the <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) information for which the registration is to be removed. The group that the registration is removed for is specified by the <b>dwGroupId</b> member in the <i>pInfo</i>.


## -returns



If the function succeeds, the return value is nonzero (TRUE).

If the function fails, the return value is zero (FALSE).




## -see-also




<a href="https://msdn.microsoft.com/557436b4-f7f1-4708-acc7-c6b47e6322ad">ALG_ID</a>



<a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a>



<a href="https://msdn.microsoft.com/06ba0f60-778d-450b-8f71-23471b8c4e2c">CRYPT_OID_INFO</a>



<a href="https://msdn.microsoft.com/87acf207-d109-4173-9530-8cbbebb473b2">CryptFindOIDInfo</a>



<a href="https://msdn.microsoft.com/7a5b4800-3182-4cd4-b17a-c6d4e11f7047">CryptRegisterOIDInfo</a>



<a href="cryptography_functions.htm">OID Support Functions</a>
 

 

