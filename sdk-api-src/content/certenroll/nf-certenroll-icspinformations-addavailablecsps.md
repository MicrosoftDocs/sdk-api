---
UID: NF:certenroll.ICspInformations.AddAvailableCsps
title: ICspInformations::AddAvailableCsps
author: windows-sdk-content
description: Adds the providers installed on the computer to the collection.
old-location: security\icspinformations_addavailablecsps_method.htm
tech.root: seccertenroll
ms.assetid: f44af323-41fb-46d6-88ed-15d465fc8815
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AddAvailableCsps, AddAvailableCsps method [Security], AddAvailableCsps method [Security],ICspInformations interface, ICspInformations interface [Security],AddAvailableCsps method, ICspInformations.AddAvailableCsps, ICspInformations::AddAvailableCsps, certenroll/ICspInformations::AddAvailableCsps, security.icspinformations_addavailablecsps_method
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
 - ICspInformations.AddAvailableCsps
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICspInformations::AddAvailableCsps


## -description


The <b>AddAvailableCsps</b> method adds the providers installed on the computer to the collection. This method is web enabled.


## -parameters






## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.

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



The <a href="https://msdn.microsoft.com/en-us/library/Aa375968(v=VS.85).aspx">ICspInformations</a> collection must be empty before you call this method.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa375967(v=VS.85).aspx">ICspInformation</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375968(v=VS.85).aspx">ICspInformations</a>
 

 

