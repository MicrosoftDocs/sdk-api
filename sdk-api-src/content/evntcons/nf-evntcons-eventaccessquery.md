---
UID: NF:evntcons.EventAccessQuery
title: EventAccessQuery function (evntcons.h)
description: Retrieves the permissions for the specified controller or provider.
helpviewer_keywords: ["EventAccessQuery","EventAccessQuery function [ETW]","base.eventaccessquery_func","etw.eventaccessquery_func","evntcons/EventAccessQuery"]
old-location: etw\eventaccessquery_func.htm
tech.root: ETW
ms.assetid: 21c87137-0e8f-43d1-9dad-9f2b4fc591a3
ms.date: 12/05/2018
ms.keywords: EventAccessQuery, EventAccessQuery function [ETW], base.eventaccessquery_func, etw.eventaccessquery_func, evntcons/EventAccessQuery
req.header: evntcons.h
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EventAccessQuery
 - evntcons/EventAccessQuery
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-eventing-controller-l1-1-1.dll
 - api-ms-win-downlevel-advapi32-l2-1-0.dll
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l2-1-1.dll
 - sechost.dll
 - API-MS-Win-eventing-controller-l1-1-0.dll
 - kernelbase.dll
api_name:
 - EventAccessQuery
---

# EventAccessQuery function (evntcons.h)


## -description

Retrieves the permissions for the specified controller or provider.

## -parameters

### -param Guid [in]

GUID that uniquely identifies the provider or session.

### -param Buffer [in, out]

Application-allocated buffer that will contain the security descriptor of the controller or provider.

### -param BufferSize [in, out]

Size of the security descriptor buffer, in bytes. If the function succeeds, this parameter receives the size of the buffer used. If the buffer is too small, the function returns ERROR_MORE_DATA and this parameter receives the required buffer size. If the buffer size is zero on input, no data is returned in the buffer and this parameter receives the required buffer size.

## -returns

Returns ERROR_SUCCESS if successful.

The function returns the following return code if an error occurs:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The buffer is too small to receive the security descriptor. Reallocate the buffer using the size returned in <i>BufferSize</i>.

</td>
</tr>
</table>

## -remarks

If the GUID does not exist in the registry, ETW returns the default permissions for a provider or controller. For details on specifying the GUID in the registry, see <a href="/windows/desktop/api/evntcons/nf-evntcons-eventaccesscontrol">EventAccessControl</a>.

For information on accessing the components of the security descriptor, see <a href="/windows/desktop/SecAuthZ/getting-information-from-an-acl">Getting Information from an ACL</a>, the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl">GetSecurityDescriptorDacl</a>, <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl">GetSecurityDescriptorSacl</a>, and <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getace">GetAce</a> functions, and the <a href="/windows/desktop/SecAuthZ/ace">ACE</a> structure.

## -see-also

<a href="/windows/desktop/api/evntcons/nf-evntcons-eventaccesscontrol">EventAccessControl</a>



<a href="/windows/desktop/api/evntcons/nf-evntcons-eventaccessremove">EventAccessRemove</a>