---
UID: NF:indexsrv.IStemmer.GetLicenseToUse
title: IStemmer::GetLicenseToUse method
author: windows-driver-content
description: Retrieves the license information for this IStemmer implementation.
old-location: indexsrv\istemmer_getlicensetouse.htm
old-project: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefint_2ch1.htm
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: GetLicenseToUse method [Indexing Service], GetLicenseToUse method [Indexing Service], IStemmer interface, GetLicenseToUse,IStemmer.GetLicenseToUse, IStemmer, IStemmer interface [Indexing Service], GetLicenseToUse method, IStemmer::GetLicenseToUse, _idxs_IStemmer_GetLicenseToUse, indexsrv.istemmer_getlicensetouse, indexsrv/IStemmer::GetLicenseToUse
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: indexsrv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WORDREP_BREAK_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Indexsrv.h
api_name:
-	IStemmer.GetLicenseToUse
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IStemmer::GetLicenseToUse method


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/6da601c6-3742-40ad-99f2-8817f7f642b3">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

Retrieves the license information for this <a href="https://msdn.microsoft.com/3b655078-367d-4e74-aeb1-a5b5c135e88e">IStemmer</a> implementation.


## -parameters




### -param ppwcsLicense [out]

A pointer to a variable that receives a pointer to the license information.


## -returns



This method can return one of these values.

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
The operation was completed successfully.

</td>
</tr>
</table>
 




## -remarks



The Indexing Service does not enforce license restrictions. The implementation determines the storage method for the license information.






## -see-also




<a href="https://msdn.microsoft.com/3b655078-367d-4e74-aeb1-a5b5c135e88e">IStemmer</a>
 

 

