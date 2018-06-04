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

# IEnumWbemClassObject::Clone


## -description


The <b>IEnumWbemClassObject::Clone</b> method makes 
    a logical copy of the entire enumerator, retaining its current position in an enumeration. This method makes only 
    a "best effort" copy. Due to the dynamic nature of many CIM objects, it is possible that the new enumerator does 
    not enumerate the same set of objects as the source enumerator.
<div class="alert"><b>Note</b>  <p class="note">When the enumeration is initialized with the <b>WBEM_FLAG_FORWARD_ONLY</b> flag, 
     <b>IEnumWbemClassObject::Clone</b> is not 
     supported.

<p class="note">Any pending asynchronous deliveries begun by 
     <a href="https://msdn.microsoft.com/1ff82982-a2d7-4618-8488-9e4b7628012d">NextAsync</a> are not cloned.

</div><div> </div>

## -parameters




### -param ppEnum [out]

Receives a pointer to a new 
      <a href="https://msdn.microsoft.com/142ea48d-d47b-4b7b-ab84-049a54955488">IEnumWbemClassObject</a> object. The caller must call 
      <a href="_com_iunknown_release">Release</a> when the interface pointer is no longer 
      required. On error, there will not be a return of a new object.


## -returns





On error, you can call the COM function 
       <a href=" http://go.microsoft.com/fwlink/p/?linkid=119575">GetErrorInfo</a> to obtain more error 
       information. COM-specific error codes may also be returned if network problems cause you to lose the remote 
       connection to Windows Management.

The following list lists the value contained within an <b>HRESULT</b>.




## -remarks



Because the call-back to the sink might not be returned at the same authentication level as the client 
    requires, it is recommended that you use semisynchronous communication instead of asynchronous. If you require 
    asynchronous communication, see 
    <a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.

For more information about using methods semisynchronously, see 
    <a href="https://msdn.microsoft.com/142ea48d-d47b-4b7b-ab84-049a54955488">IEnumWbemClassObject</a> and 
    <a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.


#### Examples

The following code shows how to use the <b>IEnumWbemClassObject::Clone</b> method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL CloneEnum(IEnumWbemClassObject *pSrc)
{
    IEnumWbemClassObject *pCopy = 0;

    HRESULT hRes = pSrc-&gt;Clone(&amp;pCopy);

    if (hRes != WBEM_S_NO_ERROR)       // Failed to clone it.
        return FALSE;

    // Use the copy of the enumerator.
    // ...

    pCopy-&gt;Release();

    return TRUE;
}</pre>
</td>
</tr>
</table></span></div>


