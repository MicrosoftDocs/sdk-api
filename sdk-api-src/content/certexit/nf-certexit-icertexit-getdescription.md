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

# ICertExit::GetDescription


## -description


The <b>GetDescription</b> method returns a human-readable description of the exit module and its function. This method was first defined in the  <a href="https://msdn.microsoft.com/731c4f3c-20b4-4f3d-8241-a94cdf656fe5">ICertExit</a> interface.


## -parameters




### -param pstrDescription [out]

A pointer to the <b>BSTR</b> that describes the exit module.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 Returns a string that describes the exit module and its function.




## -remarks



When you write a custom exit module, implement this method.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>STDMETHODIMP
CCertExit::GetDescription(
    /* [out, retval] */ BSTR __RPC_FAR *pstrDescription)
{
    if (NULL == pstrDescription)
    {
        // Bad pointer address.
        return (E_POINTER);
    }
    if (NULL != *pstrDescription)
    {
        SysFreeString(*pstrDescription);
        *pstrDescription=NULL;
    }
    // wszMyExitModuleDesc defined elsewhere, for example:
    // #define wszMyExitModuleDesc L"My Exit Module"
    *pstrDescription = SysAllocString(wszMyExitModuleDesc);
    if (NULL == *pstrDescription)
    {
        // Not enough memory
        return ( E_OUTOFMEMORY );
    }
    // Success
    return( S_OK );
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/731c4f3c-20b4-4f3d-8241-a94cdf656fe5">ICertExit</a>



<a href="https://msdn.microsoft.com/a9d66aeb-b596-4d50-9c07-b760cdf4f8c0">ICertExit2</a>
 

 

