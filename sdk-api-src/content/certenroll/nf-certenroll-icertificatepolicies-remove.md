---
UID: NF:certenroll.ICertificatePolicies.Remove
title: ICertificatePolicies::Remove
author: windows-driver-content
description: Removes an object from the collection by index number.
old-location: security\icertificatepolicies_remove_method.htm
old-project: SecCertEnroll
ms.assetid: 5cd010bb-50ee-4251-815e-1fb4de1f2a81
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: ICertificatePolicies interface [Security],Remove method, ICertificatePolicies.Remove, ICertificatePolicies::Remove, Remove, Remove method [Security], Remove method [Security],ICertificatePolicies interface, certenroll/ICertificatePolicies::Remove, security.icertificatepolicies_remove_method
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
-	ICertificatePolicies.Remove
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ICertificatePolicies::Remove


## -description


The <b>Remove</b> method removes an object from the collection by index number.


## -parameters




### -param Index [in]

A <b>LONG</b> variable that contains the index of the object to remove.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/2503adcb-0b73-42ef-98cf-a2b906e34ef7">ICertificatePolicies</a>



<a href="https://msdn.microsoft.com/2162de70-edcc-4f01-807d-79ff200d0016">ICertificatePolicy</a>
 

 

