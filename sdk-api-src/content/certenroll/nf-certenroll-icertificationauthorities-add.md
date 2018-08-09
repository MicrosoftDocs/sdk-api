---
UID: NF:certenroll.ICertificationAuthorities.Add
title: ICertificationAuthorities::Add
author: windows-sdk-content
description: Adds an ICertificationAuthority object to the collection.
old-location: security\icertificationauthorities_add.htm
old-project: seccertenroll
ms.assetid: 8a618b8b-9089-4f35-afd4-b11255a26ac9
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: Add, Add method [Security], Add method [Security],ICertificationAuthorities interface, ICertificationAuthorities interface [Security],Add method, ICertificationAuthorities.Add, ICertificationAuthorities::Add, certenroll/ICertificationAuthorities::Add, security.icertificationauthorities_add
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenroll.h
api_name:
 - ICertificationAuthorities.Add
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICertificationAuthorities::Add


## -description


The <b>Add</b> method adds an <a href="https://msdn.microsoft.com/ffd64396-a258-4cf5-aca1-a61102ecf313">ICertificationAuthority</a> object to the collection.  This method is web enabled.


## -parameters




### -param pVal [in]

Pointer to an <a href="https://msdn.microsoft.com/ffd64396-a258-4cf5-aca1-a61102ecf313">ICertificationAuthority</a> object to add to the collection.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/8dad280a-1fe7-4a4b-9392-eee3aa9bcde9">ICertificationAuthorities</a>



<a href="https://msdn.microsoft.com/ffd64396-a258-4cf5-aca1-a61102ecf313">ICertificationAuthority</a>
 

 

