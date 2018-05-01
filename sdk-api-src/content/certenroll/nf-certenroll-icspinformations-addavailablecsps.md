---
UID: NF:certenroll.ICspInformations.AddAvailableCsps
title: ICspInformations::AddAvailableCsps method
author: windows-driver-content
description: Adds the providers installed on the computer to the collection.
old-location: security\icspinformations_addavailablecsps_method.htm
old-project: SecCertEnroll
ms.assetid: f44af323-41fb-46d6-88ed-15d465fc8815
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: AddAvailableCsps method [Security], AddAvailableCsps method [Security], ICspInformations interface, AddAvailableCsps,ICspInformations.AddAvailableCsps, ICspInformations, ICspInformations interface [Security], AddAvailableCsps method, ICspInformations::AddAvailableCsps, certenroll/ICspInformations::AddAvailableCsps, security.icspinformations_addavailablecsps_method
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
-	ICspInformations.AddAvailableCsps
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ICspInformations::AddAvailableCsps method


## -description


The <b>AddAvailableCsps</b> method adds the providers installed on the computer to the collection. This method is web enabled.


## -parameters






## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>HRESULT_FROM_WIN32(ERROR_INVALID_OPERATION)</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The collection is not empty.

</td>
</tr>
</table>
 




## -remarks



The <a href="https://msdn.microsoft.com/8141023c-c162-46d6-9c37-e227ce1c8761">ICspInformations</a> collection must be empty before you call this method.




## -see-also




<a href="https://msdn.microsoft.com/e337ae2c-6f86-4025-8d31-47bc5d8a4ca8">ICspInformation</a>



<a href="https://msdn.microsoft.com/8141023c-c162-46d6-9c37-e227ce1c8761">ICspInformations</a>
 

 

