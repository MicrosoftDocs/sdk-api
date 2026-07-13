---
UID: NF:winsafer.SaferGetLevelInformation
title: SaferGetLevelInformation function (winsafer.h)
description: Retrieves information about a policy level.
helpviewer_keywords: ["SaferGetLevelInformation","SaferGetLevelInformation function [Security]","SaferObjectDescription","SaferObjectFriendlyName","SaferObjectLevelId","SaferObjectScopeId","_mnp_safergetlevelinformation","security.safergetlevelinformation","winsafer/SaferGetLevelInformation"]
old-location: security\safergetlevelinformation.htm
tech.root: security
ms.assetid: cbe73ebc-bf2c-4d39-a203-78ff1a407481
ms.date: 12/05/2018
ms.keywords: SaferGetLevelInformation, SaferGetLevelInformation function [Security], SaferObjectDescription, SaferObjectFriendlyName, SaferObjectLevelId, SaferObjectScopeId, _mnp_safergetlevelinformation, security.safergetlevelinformation, winsafer/SaferGetLevelInformation
req.header: winsafer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SaferGetLevelInformation
 - winsafer/SaferGetLevelInformation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
api_name:
 - SaferGetLevelInformation
req.apiset: ext-ms-win-advapi32-safer-l1-1-0 (introduced in Windows 8)
---

# SaferGetLevelInformation function


## -description

The <b>SaferGetLevelInformation</b> function retrieves information about a policy level.

## -parameters

### -param LevelHandle [in]

The handle of the level to be queried.

### -param dwInfoType [in]

A SAFER_OBJECT_INFO_CLASS enumeration value that specifies the type of object information that should be returned.  The specified value determines the size and type of the <i>lpQueryBuffer</i> parameter. The following table shows the possible values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SaferObjectLevelId"></a><a id="saferobjectlevelid"></a><a id="SAFEROBJECTLEVELID"></a><dl>
<dt><b>SaferObjectLevelId</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Queries for the LEVELID constant.

<i>lpQueryBuffer</i> return type: <b>DWORD</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="SaferObjectScopeId"></a><a id="saferobjectscopeid"></a><a id="SAFEROBJECTSCOPEID"></a><dl>
<dt><b>SaferObjectScopeId</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Queries for the user or machine scope.

<i>lpQueryBuffer</i> return type: <b>DWORD</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="SaferObjectFriendlyName"></a><a id="saferobjectfriendlyname"></a><a id="SAFEROBJECTFRIENDLYNAME"></a><dl>
<dt><b>SaferObjectFriendlyName</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Queries for the display name.

<i>lpQueryBuffer</i> return type: <b>LPCWSTR</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="SaferObjectDescription"></a><a id="saferobjectdescription"></a><a id="SAFEROBJECTDESCRIPTION"></a><dl>
<dt><b>SaferObjectDescription</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Queries for the description.

<i>lpQueryBuffer</i> return type: <b>LPCWSTR</b>.

</td>
</tr>
</table>

### -param lpQueryBuffer [out, optional]

A buffer to contain the results of the query. For the type of the returned information for each possible value of the <i>dwInfoType</i> parameter, see the <i>dwInfoType</i> parameter.

### -param dwInBufferSize [in]

The size of the <i>lpQueryBuffer</i> parameter in bytes.

### -param lpdwOutBufferSize [out]

A pointer to return the output size of the <i>lpQueryBuffer</i> parameter.

## -returns

<b>TRUE</b> if the function succeeds; otherwise, <b>FALSE</b>. For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.
