---
UID: NF:winsafer.SaferSetLevelInformation
title: SaferSetLevelInformation function
author: windows-sdk-content
description: Sets the information about a policy level.
old-location: security\safersetlevelinformation.htm
tech.root: secmgmt
ms.assetid: 8DB13F94-1736-4C05-B072-BFBFC076A726
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: SaferObjectDescription, SaferObjectFriendlyName, SaferObjectLevelId, SaferObjectScopeId, SaferSetLevelInformation, SaferSetLevelInformation function [Security], security.safersetlevelinformation, winsafer/SaferSetLevelInformation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
api_name:
 - SaferSetLevelInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- SaferSetLevelInformation
: 
---

# SaferSetLevelInformation function


## -description


The <b>SaferSetLevelInformation</b> function sets the information about a policy level.


## -parameters




### -param LevelHandle [in]

The handle of the level to be set.


### -param dwInfoType [in]

A <a href="https://msdn.microsoft.com/31de9e42-6795-433a-937f-c4243e4961df">SAFER_OBJECT_INFO_CLASS</a> enumeration value that specifies the type of object information that should be set.  The specified value determines the size and type of the <i>lpQueryBuffer</i> parameter. The following table shows the possible values.

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
Sets the LEVELID constant.

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
Sets the user or machine scope.

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
Sets the display name.

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
Sets the description.

<i>lpQueryBuffer</i> return type: <b>LPCWSTR</b>.

</td>
</tr>
</table>
 


### -param lpQueryBuffer [in]

A buffer to contain the results of the query. For the type of the returned information for each possible value of the <i>dwInfoType</i> parameter, see the <i>dwInfoType</i> parameter.


### -param dwInBufferSize [in]

The size, in bytes, of the <i>lpQueryBuffer</i> parameter.


## -returns



<b>TRUE</b> if the function succeeds; otherwise, <b>FALSE</b>. For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.



