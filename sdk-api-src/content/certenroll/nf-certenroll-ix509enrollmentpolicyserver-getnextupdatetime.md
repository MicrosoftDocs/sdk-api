---
UID: NF:certenroll.IX509EnrollmentPolicyServer.GetNextUpdateTime
title: IX509EnrollmentPolicyServer::GetNextUpdateTime (certenroll.h)
description: Retrieves the date and time at which the policy expires and should be refreshed.
helpviewer_keywords: ["GetNextUpdateTime","GetNextUpdateTime method [Security]","GetNextUpdateTime method [Security]","IX509EnrollmentPolicyServer interface","IX509EnrollmentPolicyServer interface [Security]","GetNextUpdateTime method","IX509EnrollmentPolicyServer.GetNextUpdateTime","IX509EnrollmentPolicyServer::GetNextUpdateTime","certenroll/IX509EnrollmentPolicyServer::GetNextUpdateTime","security.ix509enrollmentpolicyserver_getnextupdatetime"]
old-location: security\ix509enrollmentpolicyserver_getnextupdatetime.htm
tech.root: security
ms.assetid: 23ddd933-2392-410b-a4e6-7f5c00f867b3
ms.date: 12/05/2018
ms.keywords: GetNextUpdateTime, GetNextUpdateTime method [Security], GetNextUpdateTime method [Security],IX509EnrollmentPolicyServer interface, IX509EnrollmentPolicyServer interface [Security],GetNextUpdateTime method, IX509EnrollmentPolicyServer.GetNextUpdateTime, IX509EnrollmentPolicyServer::GetNextUpdateTime, certenroll/IX509EnrollmentPolicyServer::GetNextUpdateTime, security.ix509enrollmentpolicyserver_getnextupdatetime
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IX509EnrollmentPolicyServer::GetNextUpdateTime
 - certenroll/IX509EnrollmentPolicyServer::GetNextUpdateTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenroll.h
api_name:
 - IX509EnrollmentPolicyServer.GetNextUpdateTime
---

# IX509EnrollmentPolicyServer::GetNextUpdateTime


## -description

The <b>GetNextUpdateTime</b> method retrieves the date and time at which the policy expires and should be refreshed.

## -parameters

### -param pDate [out, retval]

Pointer to a <b>DATE</b> value that identifies the time.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table.  For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CERTSRV_E_PROPERTY_EMPTY</b></dt>
</dl>
</td>
<td width="60%">
The value could not be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pDate</i> parameter cannot be <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The date is stored as an 8-byte real value that represents a Coordinated Universal Time (Greenwich Mean Time) value between January 1, 1900 and December 31, 9999, inclusive. The value 2.0 represents January 1, 1900; 3.0 represents January 2, 1900. Adding 1 to the value increments the date by a day. The fractional part of the value represents the time of day. Therefore, 2.5 represents 12:00 on January 1, 1900; 3.25 represents 06:00 on January 2, 1900.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollmentpolicyserver">IX509EnrollmentPolicyServer</a>