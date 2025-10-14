---
UID: NF:certenroll.ICspInformations.AddAvailableCsps
title: ICspInformations::AddAvailableCsps (certenroll.h)
description: Adds the providers installed on the computer to the collection.
helpviewer_keywords: ["AddAvailableCsps","AddAvailableCsps method [Security]","AddAvailableCsps method [Security]","ICspInformations interface","ICspInformations interface [Security]","AddAvailableCsps method","ICspInformations.AddAvailableCsps","ICspInformations::AddAvailableCsps","certenroll/ICspInformations::AddAvailableCsps","security.icspinformations_addavailablecsps_method"]
old-location: security\icspinformations_addavailablecsps_method.htm
tech.root: security
ms.assetid: f44af323-41fb-46d6-88ed-15d465fc8815
ms.date: 12/05/2018
ms.keywords: AddAvailableCsps, AddAvailableCsps method [Security], AddAvailableCsps method [Security],ICspInformations interface, ICspInformations interface [Security],AddAvailableCsps method, ICspInformations.AddAvailableCsps, ICspInformations::AddAvailableCsps, certenroll/ICspInformations::AddAvailableCsps, security.icspinformations_addavailablecsps_method
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICspInformations::AddAvailableCsps
 - certenroll/ICspInformations::AddAvailableCsps
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - ICspInformations.AddAvailableCsps
---

# ICspInformations::AddAvailableCsps


## -description

The <b>AddAvailableCsps</b> method adds the providers installed on the computer to the collection. This method is web enabled.



## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_OPERATION)</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The collection is not empty.

</td>
</tr>
</table>

## -remarks

The <a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformations">ICspInformations</a> collection must be empty before you call this method.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformations">ICspInformations</a>
