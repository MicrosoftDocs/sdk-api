---
UID: NF:certenroll.ICspStatuses.Add
title: ICspStatuses::Add
author: windows-sdk-content
description: Adds an ICspStatus object to the collection.
old-location: security\icspstatuses_add_method.htm
tech.root: SecCertEnroll
ms.assetid: f8238071-f2e4-4533-b9bc-a86cea8086a5
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Add, Add method [Security], Add method [Security],ICspStatuses interface, ICspStatuses interface [Security],Add method, ICspStatuses.Add, ICspStatuses::Add, certenroll/ICspStatuses::Add, security.icspstatuses_add_method
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - ICspStatuses.Add
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
- ICspStatuses.Add
: 
---

# ICspStatuses::Add


## -description


The <b>Add</b> method adds an <a href="https://msdn.microsoft.com/en-us/library/Aa376760(v=VS.85).aspx">ICspStatus</a> object to the collection. This method is web enabled.


## -parameters




### -param pVal [in]

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/Aa376760(v=VS.85).aspx">ICspStatus</a> object to add to the collection.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa376760(v=VS.85).aspx">ICspStatus</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa376761(v=VS.85).aspx">ICspStatuses</a>
 

 

