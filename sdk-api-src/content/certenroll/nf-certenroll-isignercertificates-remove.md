---
UID: NF:certenroll.ISignerCertificates.Remove
title: ISignerCertificates::Remove method
author: windows-driver-content
description: Removes an ISignerCertificate object from the collection by index number.
old-location: security\isignercertificates_remove_method.htm
old-project: SecCertEnroll
ms.assetid: 3f0a3d9b-590f-4fa2-904c-26593bf977c8
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: ISignerCertificates, ISignerCertificates interface [Security], Remove method, ISignerCertificates::Remove, Remove method [Security], Remove method [Security], ISignerCertificates interface, Remove,ISignerCertificates.Remove, certenroll/ISignerCertificates::Remove, security.isignercertificates_remove_method
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
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CertEnroll.dll
api_name:
-	ISignerCertificates.Remove
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ISignerCertificates::Remove method


## -description


The <b>Remove</b> method removes an <a href="https://msdn.microsoft.com/146a1925-4de6-492c-8014-612c65bd7270">ISignerCertificate</a> object from the collection by index number.


## -parameters




### -param Index [in]

A <b>LONG</b> variable that contains the index of the object to remove.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/146a1925-4de6-492c-8014-612c65bd7270">ISignerCertificate</a>



<a href="https://msdn.microsoft.com/420d6550-514a-4fea-987b-6deecbc9b717">ISignerCertificates</a>
 

 

