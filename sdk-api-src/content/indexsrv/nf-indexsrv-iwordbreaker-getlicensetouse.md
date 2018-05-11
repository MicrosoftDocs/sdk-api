---
UID: NF:indexsrv.IWordBreaker.GetLicenseToUse
title: IWordBreaker::GetLicenseToUse
author: windows-driver-content
description: Retrieves a pointer to the license information for this implementation of the IWordBreaker interface.
old-location: indexsrv\iwordbreaker_getlicensetouse.htm
old-project: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefint_7vvp.htm
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: GetLicenseToUse, GetLicenseToUse method [Indexing Service], GetLicenseToUse method [Indexing Service],IWordBreaker interface, IWordBreaker interface [Indexing Service],GetLicenseToUse method, IWordBreaker.GetLicenseToUse, IWordBreaker::GetLicenseToUse, _idxs_IWordBreaker_GetLicenseToUse, indexsrv.iwordbreaker_getlicensetouse, indexsrv/IWordBreaker::GetLicenseToUse
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
-	IWordBreaker.GetLicenseToUse
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IWordBreaker::GetLicenseToUse


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/6da601c6-3742-40ad-99f2-8817f7f642b3">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

Retrieves a pointer to the license information for this implementation of the <a href="https://msdn.microsoft.com/994befe1-e258-4c0a-b3a9-b5968e13456c">IWordBreaker</a> interface.


## -parameters




### -param ppwcsLicense [out]

A pointer to an output variable. The output variable receives a pointer to the license information for this <a href="https://msdn.microsoft.com/994befe1-e258-4c0a-b3a9-b5968e13456c">IWordBreaker</a> implementation. 



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
 




## -see-also




<a href="https://msdn.microsoft.com/994befe1-e258-4c0a-b3a9-b5968e13456c">IWordBreaker</a>
 

 

