---
UID: NF:certenroll.ICertificationAuthorities.Remove
title: ICertificationAuthorities::Remove
author: windows-sdk-content
description: Removes an ICertificationAuthority object from the collection by index number.
old-location: security\icertificationauthorities_remove.htm
old-project: SecCertEnroll
ms.assetid: 97fb196f-eba0-4d73-b89b-f2eb477747fe
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: ICertificationAuthorities interface [Security],Remove method, ICertificationAuthorities.Remove, ICertificationAuthorities::Remove, Remove, Remove method [Security], Remove method [Security],ICertificationAuthorities interface, certenroll/ICertificationAuthorities::Remove, security.icertificationauthorities_remove
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Certenroll.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Certenroll.h
api_name:
-	ICertificationAuthorities.Remove
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICertificationAuthorities::Remove


## -description


The <b>Remove</b> method removes an <a href="https://msdn.microsoft.com/ffd64396-a258-4cf5-aca1-a61102ecf313">ICertificationAuthority</a> object from the collection by index number.


## -parameters




### -param Index [in]

A <b>LONG</b> variable that contains the index of the object to remove.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/8dad280a-1fe7-4a4b-9392-eee3aa9bcde9">ICertificationAuthorities</a>



<a href="https://msdn.microsoft.com/ffd64396-a258-4cf5-aca1-a61102ecf313">ICertificationAuthority</a>
 

 

