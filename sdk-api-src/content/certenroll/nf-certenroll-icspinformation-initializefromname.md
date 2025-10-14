---
UID: NF:certenroll.ICspInformation.InitializeFromName
title: ICspInformation::InitializeFromName (certenroll.h)
description: Initializes the object from a string that contains a provider name.
helpviewer_keywords: ["ICspInformation interface [Security]","InitializeFromName method","ICspInformation.InitializeFromName","ICspInformation::InitializeFromName","InitializeFromName","InitializeFromName method [Security]","InitializeFromName method [Security]","ICspInformation interface","certenroll/ICspInformation::InitializeFromName","security.icspinformation_initializefromname_method"]
old-location: security\icspinformation_initializefromname_method.htm
tech.root: security
ms.assetid: b405503f-2af5-4a2f-abdb-e2eb108c4b1b
ms.date: 12/05/2018
ms.keywords: ICspInformation interface [Security],InitializeFromName method, ICspInformation.InitializeFromName, ICspInformation::InitializeFromName, InitializeFromName, InitializeFromName method [Security], InitializeFromName method [Security],ICspInformation interface, certenroll/ICspInformation::InitializeFromName, security.icspinformation_initializefromname_method
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
 - ICspInformation::InitializeFromName
 - certenroll/ICspInformation::InitializeFromName
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
 - ICspInformation.InitializeFromName
---

# ICspInformation::InitializeFromName


## -description

The <b>InitializeFromName</b> method initializes the object from a string that contains a provider name. This method is web enabled.

## -parameters

### -param strName [in]

A <b>BSTR</b> variable that contains the name.

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
<dt><b>HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The object is already initialized.

</td>
</tr>
</table>

## -remarks

The <b>InitializeFromName</b> method opens the named provider and queries it to set the following property values on the <a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a> object:<ul>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-icspinformation-get_cspalgorithms">CspAlgorithms</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-icspinformation-get_hashardwarerandomnumbergenerator">HasHardwareRandomNumberGenerator</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-icspinformation-get_ishardwaredevice">IsHardwareDevice</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-icspinformation-get_isremovable">IsRemovable</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-icspinformation-get_issmartcard">IsSmartCard</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-icspinformation-get_issoftwaredevice">IsSoftwareDevice</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-icspinformation-get_keyspec">KeySpec</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-icspinformation-get_legacycsp">LegacyCsp</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-icspinformation-get_maxkeycontainernamelength">MaxKeyContainerNameLength</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-icspinformation-get_name">Name</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-icspinformation-get_type">Type</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-icspinformation-get_valid">Valid</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-icspinformation-get_version">Version</a>
</li>
</ul>


The method adds the available algorithms to the <a href="/windows/desktop/api/certenroll/nn-certenroll-icspalgorithms">ICspAlgorithms</a> collection returned by the <a href="/windows/desktop/api/certenroll/nf-certenroll-icspinformation-get_cspalgorithms">CspAlgorithms</a> property. Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-icspinformation-initializefromtype">InitializeFromType</a> method to initialize the object from a provider type.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a>