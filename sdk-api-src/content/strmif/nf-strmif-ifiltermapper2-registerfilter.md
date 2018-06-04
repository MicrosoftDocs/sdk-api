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

# IFilterMapper2::RegisterFilter


## -description



The <code>RegisterFilter</code> method adds filter information to the registry.




## -parameters




### -param clsidFilter [in]

Class identifier (CLSID) of the filter.


### -param Name [in]

Descriptive name for the filter.


### -param ppMoniker [in, out]

Address of a pointer to a device moniker that determines where this filter's data will be written. Can be <b>NULL</b>.


### -param pclsidCategory [in]

Pointer to the filter category of the filter. If <b>NULL</b>, the default category is CLSID_ActiveMovieFilters. (See <a href="https://msdn.microsoft.com/cab4e2c9-eab9-4836-adfc-870490ca5b6b">Filter Categories</a>.)


### -param szInstance [in]

Instance data for constructing the device moniker's display name. Can be the friendly name, or the string representation of the filter CLSID. If <b>NULL</b>, defaults to the filter CLSID.


### -param prf2 [in]

Pointer to a <a href="https://msdn.microsoft.com/651b94e6-b343-4957-9781-768b04c098dd">REGFILTER2</a> structure containing filter information.


## -returns



Returns an <b>HRESULT</b> value. Possible values include those shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_BAD_KEY</b></dt>
</dl>
</td>
<td width="60%">
Could not get registry key.

</td>
</tr>
</table>
 




## -remarks



This method adds information about the filter to the registry, under the registry entry for the specified filter category. It does not register the in-process server that creates the filter (usually a DLL). To register the server, you can call the <a href="https://msdn.microsoft.com/2122949d-0117-4c68-bfcd-c717b14dc970">AMovieDllRegisterServer2</a> function.

For the <i>ppMoniker</i> parameter, use one of the following:

<ul>
<li>The address of an <a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a> interface pointer for an existing device moniker</li>
<li>The address of a <b>NULL</b><b>IMoniker</b> interface pointer</li>
<li><b>NULL</b></li>
</ul>
If you are registering a filter for a Windows Driver Model (WDM) or Plug and Play device, pass the address of the existing device moniker. The filter will be registered using this moniker. When the method returns, <i>*ppMoniker</i> is set to <b>NULL</b>.

Otherwise, the method creates a new moniker. If <i>ppMoniker</i> is non-<b>NULL</b>, the method sets <i>*ppMoniker</i> to point to the new moniker. The application can use this moniker to write additional private values in the property bag. Be sure to release the interface.

Set <i>ppMoniker</i> to <b>NULL</b> if you don't want to provide or receive the moniker.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/6a3db838-cee3-4a9f-a924-fb55931acc83">IFilterMapper2 Interface</a>
 

 

