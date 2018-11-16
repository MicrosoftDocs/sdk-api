---
UID: NF:certenroll.ICertificationAuthorities.Add
title: ICertificationAuthorities::Add
author: windows-sdk-content
description: Adds an ICertificationAuthority object to the collection.
old-location: security\icertificationauthorities_add.htm
tech.root: SecCertEnroll
ms.assetid: 8a618b8b-9089-4f35-afd4-b11255a26ac9
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Add, Add method [Security], Add method [Security],ICertificationAuthorities interface, ICertificationAuthorities interface [Security],Add method, ICertificationAuthorities.Add, ICertificationAuthorities::Add, certenroll/ICertificationAuthorities::Add, security.icertificationauthorities_add
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- certenroll.h
: 
- ICertificationAuthorities.Add
: 
---

# ICertificationAuthorities::Add


## -description


The <b>Add</b> method adds an <a href="https://msdn.microsoft.com/en-us/library/Ee338621(v=VS.85).aspx">ICertificationAuthority</a> object to the collection.  This method is web enabled.


## -parameters




### -param pVal [in]

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/Ee338621(v=VS.85).aspx">ICertificationAuthority</a> object to add to the collection.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ee338611(v=VS.85).aspx">ICertificationAuthorities</a>



<a href="https://msdn.microsoft.com/en-us/library/Ee338621(v=VS.85).aspx">ICertificationAuthority</a>
 

 

