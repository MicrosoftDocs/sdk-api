---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IAzClientContext2::GetAssignedScopesPage


## -description


The <b>GetAssignedScopesPage</b> method retrieves a list of the scopes in which the client represented by the current <a href="https://msdn.microsoft.com/8e922370-18e3-481c-93f2-9a56d7898ba7">IAzClientContext2</a> object is assigned to at least one role.


## -parameters




### -param lOptions [in]

A flag that specifies whether this method checks LDAP query groups for scope assignment. Previously cached LDAP query groups are checked regardless of the value of this flag.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AZ_CLIENT_CONTEXT_SKIP_LDAP_QUERY"></a><a id="az_client_context_skip_ldap_query"></a><dl>
<dt><b>AZ_CLIENT_CONTEXT_SKIP_LDAP_QUERY</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
LDAP query groups that were not previously cached are not checked.

</td>
</tr>
</table>
 


### -param PageSize [in]

The number of elements in each page result.


### -param pvarCursor [in, out]

A pointer to a <b>VARIANT</b> that represents the current page of results. For the first call to the  <b>GetAssignedScopesPage</b> method, pass <b>VT_EMPTY</b> as the value for this parameter to retrieve the first page of results. The number of elements on a page is determined by the value of the <i>PageSize</i> parameter. On output, this parameter contains the value to be passed in the next call to <b>GetAssignedScopesPage</b> to retrieve the next page of results. If the value of this parameter on output is <b>EMPTY</b>, there are no more result pages.


### -param pvarScopeNames

On return, contains an array of variables of type <b>VARIANT</b>. Each element of the array is of type <b>VT_BSTR</b> and contains the name of a scope to which the current client is assigned. The number of elements in the array is specified by the <i>PageSize</i> parameter.


## -returns



If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



If multiple threads access the same authorization store, a call to the  <b>GetAssignedScopesPage</b> method on one of the threads might not return accurate results if the other thread modifies the store.

In  JScript, the returned <a href="9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY</a> values must be converted to the JScript <a href="08e5f552-0797-4b48-8164-609582fc18c9">Array</a> object.



