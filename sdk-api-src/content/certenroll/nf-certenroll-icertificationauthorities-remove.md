---
UID: NF:certenroll.ICertificationAuthorities.Remove
title: ICertificationAuthorities::Remove
author: windows-sdk-content
description: Removes an ICertificationAuthority object from the collection by index number.
old-location: security\icertificationauthorities_remove.htm
tech.root: SecCertEnroll
ms.assetid: 97fb196f-eba0-4d73-b89b-f2eb477747fe
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ICertificationAuthorities interface [Security],Remove method, ICertificationAuthorities.Remove, ICertificationAuthorities::Remove, Remove, Remove method [Security], Remove method [Security],ICertificationAuthorities interface, certenroll/ICertificationAuthorities::Remove, security.icertificationauthorities_remove
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
 - ICertificationAuthorities.Remove
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
- ICertificationAuthorities.Remove
: 
---

# ICertificationAuthorities::Remove


## -description


The <b>Remove</b> method removes an <a href="https://msdn.microsoft.com/en-us/library/Ee338621(v=VS.85).aspx">ICertificationAuthority</a> object from the collection by index number.


## -parameters




### -param Index [in]

A <b>LONG</b> variable that contains the index of the object to remove.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ee338611(v=VS.85).aspx">ICertificationAuthorities</a>



<a href="https://msdn.microsoft.com/en-us/library/Ee338621(v=VS.85).aspx">ICertificationAuthority</a>
 

 

