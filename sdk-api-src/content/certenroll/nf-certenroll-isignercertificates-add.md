---
UID: NF:certenroll.ISignerCertificates.Add
title: ISignerCertificates::Add
author: windows-sdk-content
description: Adds an ISignerCertificate object to the collection.
old-location: security\isignercertificates_add_method.htm
tech.root: seccertenroll
ms.assetid: 985bda2c-caad-4910-9e9c-d673975953aa
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: Add, Add method [Security], Add method [Security],ISignerCertificates interface, ISignerCertificates interface [Security],Add method, ISignerCertificates.Add, ISignerCertificates::Add, certenroll/ISignerCertificates::Add, security.isignercertificates_add_method
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
 - ISignerCertificates.Add
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISignerCertificates::Add


## -description


The <b>Add</b> method adds an <a href="https://msdn.microsoft.com/en-us/library/Aa376820(v=VS.85).aspx">ISignerCertificate</a> object to the collection.


## -parameters




### -param pVal [in]

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/Aa376820(v=VS.85).aspx">ISignerCertificate</a> object to add to the collection.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa376820(v=VS.85).aspx">ISignerCertificate</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa376821(v=VS.85).aspx">ISignerCertificates</a>
 

 

