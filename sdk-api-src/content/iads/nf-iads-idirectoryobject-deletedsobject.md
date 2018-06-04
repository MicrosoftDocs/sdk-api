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

# IDirectoryObject::DeleteDSObject


## -description


The <b>IDirectoryObject::DeleteDSObject</b> method deletes a leaf object in a directory tree.


## -parameters




### -param pszRDNName

The relative distinguished name (relative path) of the object to be deleted.


## -returns



This method returns the standard return values, including S_OK for a successful operation. For more information and other return values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



To delete a container object and its children, use the  <a href="https://msdn.microsoft.com/53685f60-9adf-40f0-b6d3-e59a0435f744">IADsDeleteOps::DeleteObject</a> method.


#### Examples

The following C/C++ code example shows how to delete a user object.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT hr;
IDirectoryObject *pDirObject=NULL;
hr = ADsGetObject(L"LDAP://OU=Sales,DC=Fabrikam,DC=com",
    IID_IDirectoryObject, (void**) &amp;pDirObject );
 
if ( SUCCEEDED(hr) )
{
    hr = pDirObject-&gt;DeleteDSObject( L"CN=Jeff Smith" );

    pDirObject-&gt;Release();
} 
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/53685f60-9adf-40f0-b6d3-e59a0435f744">IADsDeleteOps::DeleteObject</a>



<a href="https://msdn.microsoft.com/bc4f8920-2881-4393-bb01-ed837c3db6ad">IDirectoryObject</a>
 

 

