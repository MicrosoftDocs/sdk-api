---
UID: NF:certenroll.ISignerCertificates.Remove
title: ISignerCertificates::Remove
author: windows-sdk-content
description: Removes an ISignerCertificate object from the collection by index number.
old-location: security\isignercertificates_remove_method.htm
tech.root: SecCertEnroll
ms.assetid: 3f0a3d9b-590f-4fa2-904c-26593bf977c8
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ISignerCertificates interface [Security],Remove method, ISignerCertificates.Remove, ISignerCertificates::Remove, Remove, Remove method [Security], Remove method [Security],ISignerCertificates interface, certenroll/ISignerCertificates::Remove, security.isignercertificates_remove_method
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
 - ISignerCertificates.Remove
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISignerCertificates::Remove


## -description


The <b>Remove</b> method removes an <a href="https://msdn.microsoft.com/en-us/library/Aa376820(v=VS.85).aspx">ISignerCertificate</a> object from the collection by index number.


## -parameters




### -param Index [in]

A <b>LONG</b> variable that contains the index of the object to remove.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa376820(v=VS.85).aspx">ISignerCertificate</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa376821(v=VS.85).aspx">ISignerCertificates</a>
 

 

